##### Pārbaudīt kāds commit hash ir lokālajā git repozitorijā un salīdzināt to ar šī paša faila commit hash github.

```sh
commit 27d84652c9cb04f7336a7d3c35b10e622d9f7fd8
Author: Martins Abele <martins.abelis@gmail.com>
Date:   Wed Apr 27 22:43:32 2022 +0300

added module_1 README
```

github:
commit 27d84652c9cb04f7336a7d3c35b10e622d9f7fd8

##### Salīdzināt vienādu failu (ne README) hash no mapes module_1 un module_2. Vai git redz atšķirību starp šiem failiem?

Git uztver failus kā vienādus.

```sh
martins@martins-Vostro-5568:~/git_repos/devops$ git hash-object ./module_1/image-007.jpg
3dc9cce67ad44b6fe1c3b4b948a49d66c55d302a
martins@martins-Vostro-5568:~/git_repos/devops$ git hash-object ./module_2/image-007.jpg
3dc9cce67ad44b6fe1c3b4b948a49d66c55d302a
```

##### Pārbaudīt kādas izmaiņas tika veiktas iepriekšējās nedēļas laikā. Atrast vismaz divus veidus kā to izdarīt.
```sh
$ git log --since=1.week
$ git log --since="2022-04-21"
$ git log --since="1 week ago"
```

Atrast commit kurus veica autors - “Laura Pacilio”

```sh
$ git log --author "Laura Pacilio"
```

Atrast vai Laura ir veikusi commit pagājušā gada septembrī? Jā, ir veikusi.

```sh
git log --author "Laura Pacilio" --since="last year august" --until="last year september"
```

Vai Laura ir veikusi commit vakar? Nav veikusi.

```sh
$ git log --author "Laura Pacilio" --since=2.days --until=1.day
```


