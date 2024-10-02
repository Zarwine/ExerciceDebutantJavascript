```php

public class Oiseau {
  string $nickname = "bab";

  __construct($nickname = "bob") {
    $this->nickname = $nickname;
  }

  /**
   * Donne le nom de l'oiseau pardi ! 
   */
  public function getNickname(): string
  {
    return $this->nickname;
  }

  /**
   * Change le nom de l'oiseau
   */
  public function setNickname(?string $nickname): void
  {
    $this->nickname = $nickname;
  }
}
```

Quels sont les résultats suivant ? Comment s'appellent les oiseaux?
```php
$oiseau1 = new Oiseau();
dump($oiseau1->getNickname());

$oiseau2 = new Oiseau("cuicui");
dump($oiseau2->getNickname());

$oiseau3 = new Oiseau("cuicui");
$oiseau3->setNickname("JE SUIS UNE PATATE !!");
dump($oiseau3->getNickname());


$oiseau4 = new Oiseau("cuicui");
$oiseau4->setNickname(null);
dump($oiseau4->getNickname());
```
