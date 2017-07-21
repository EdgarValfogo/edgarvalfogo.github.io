---
layout: post
title:  "Verificando se uma tabela existe | Wordpress"
date:   2017-07-21 14:00:00 -0300
categories: wordpress
---

## Preciso verificar se uma tabela existe! E agora, José?

Quando desenvolvemos temas e plugins para Wordpress que acabam necessitando de uma funcionalidade que por sua vez necessitam de armazenamento, temos também que pensar na reutilização, na reinstalação, manutenibilidade, entre outros 1001 itens de um bom desenvolvimento.

*Dai chega aquele momento lindo de verificar se a tabela é existente na nossa DB do wordpress*

A base do código é:

```php?start_inline=true
//Carregar o objeto que gerencia o banco de dados, $wpdb
global $wpdb; 

//Armazenar o nome da tabela em uma variável para facilitar a verificação, e a reutilização do mesmo.
$table_name = $wpdb->prefix.'minha_tabela';

if($wpdb->get_var("SHOW TABLES LIKE '$table_name'") != $table_name) {
  //No caso da tabela não estar criada ...
}
else{
  //No caso da tabela já estar criada ...
}
```

Depois dá uma olhadinha no [Codex do Wordpress, referente ao $wpdb][wp-docs] caso não tenha visto ainda. É bem útil.

## Exemplo de aplicação:

No meu tema atual, gostaria que uma tabela fosse criada, especialmente para o uso de certa função, digamos que a função que vai armazenar certos dados, para a reutilização no tema, em fragmentos específicos.

Logo, tenho que pensar em hooks, pois devo verificar isso na instalação do tema e também dar um **re-check** pra ter certeza né.

Vou pensar em criar uma função para reaproveitar a verificação nos hooks e outra para criar a tabela. Vou adicionar os fragmentos de código a seguir no **functions.php**, o nosso queridinho por fazer estas chamadas tão importantes. 
[Saiba mais sbore o **functions.php** aqui][functions-docs]

### As funções:
```php?start_inline=true
function create_custom_table() {
  $table_name = $wpdb->prefix . "minha_tabela";

  global $wpdb;

  // Vamos adquirir o collation pré-configurado no nosso WP
  $collate = $wpdb->get_charset_collate();

  $sql = "CREATE TABLE {$table_name} (
    id mediumint(9) NOT NULL AUTO_INCREMENT,
    campo_1 text NOT NULL,
    campo_2 text NOT NULL,
    UNIQUE KEY id (id)
  ) $collate;";

  // Este requerimento vai possibilitar a execução do dbDelta, função que executará a query sql
  require_once( ABSPATH . 'wp-admin/includes/upgrade.php' );

  dbDelta( $sql );
}

function check_custom_table() {
  $table_name = $wpdb->prefix . "minha_tabela";

  if( $wpdb->get_var("SHOW TABLES LIKE '{$table_name}'" ) != $table_name) {
    create_custom_table();
  }
}
```

Sobre o arquivos que fizemos a requisição, [saiba mais sobre ele aqui.][upgrade-docs]

Agora temos uma função para criar a tabela, e outra para verificar se ela existe.

### Os hooks
Ainda dentro de functions.php
```php?start_inline=true
  
  function my_theme_verifications() {
    // [...] Vamos supor que você faz aqui uma série de instruções
    // E também verifica a sua tabela que é tão importante para o 
    // funcionamento do seu tema:
    check_custom_table();
  }

  add_action('after_setup_theme', 'my_theme_verifications');
```

### O snippet completo:
```php?start_inline=true
  function create_custom_table() {
    $table_name = $wpdb->prefix . "minha_tabela";

    global $wpdb;

    // Vamos adquirir o collation pré-configurado no nosso WP
    $collate = $wpdb->get_charset_collate();

    $sql = "CREATE TABLE {$table_name} (
      id mediumint(9) NOT NULL AUTO_INCREMENT,
      campo_1 text NOT NULL,
      campo_2 text NOT NULL,
      UNIQUE KEY id (id)
    ) $collate;";

    // Este requerimento vai possibilitar a execução do dbDelta, função que executará a query sql
    require_once( ABSPATH . 'wp-admin/includes/upgrade.php' );

    dbDelta( $sql );
  }

  function check_custom_table() {
    $table_name = $wpdb->prefix . "minha_tabela";

    if( $wpdb->get_var("SHOW TABLES LIKE '{$table_name}'" ) != $table_name) {
      create_custom_table();
    }
  }
  
  function my_theme_verifications() {
    // [...] Vamos supor que você faz aqui uma série de instruções
    // E também verifica a sua tabela que é tão importante para o 
    // funcionamento do seu tema:
    check_custom_table();
  }

  add_action('after_setup_theme', 'my_theme_verifications');
```

E é isso aí, espero ajudar alguém que vaga procurando uma ajudinha na criação de temas e plugins para wordpress.

Abraços, caros **dev-amiguinhos**!

[wp-docs]: https://codex.wordpress.org/Class_Reference/wpdb
[functions-docs]: https://codex.wordpress.org/Functions_File_Explained
[upgrade-docs]: https://developer.wordpress.org/reference/functions/dbdelta/