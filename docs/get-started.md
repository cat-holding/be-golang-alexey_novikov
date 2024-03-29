# Начало работы — язык программирования Go

## Шаг 1: Инициализация нового модуля в проекте

В терминале необходимо открыть корневую директорию проекта и ввести следующую команду:

```bash
go mod init <module_name>
```

После выполнения команды в каталоге проекта будет сгенерирован новый файл с именем `go.mod`.

> Файл `go.mod` содержит такую ​​информацию, как имя модуля проекта, используемую версию Go, и список сторонних модулей Go.


#### Как выбрать название для модуля Go?

Когда вы инициализируете свой модуль Go, лучше всего дать вашему модулю имя домена вашего сайта (например `site.com`).

Или в качестве альтернативы использовать путь к репозиторию `github.com/<название-профиля>/<название-репозитория>`. Имя модуля Go важно, потому что оно будет использоваться при попытке доступа к локальным пакетам Go.


## Шаг 2: Создание программы выводящей фразу «Hello, World!»

Создайте файл `main.go` и введите следующий исходный код:

```go
package main

import "fmt"

func main() {
  fmt.Println("Hello, World!")
}
```

`package` — это ключевое слово Go, определяющее, к какому пакету кода принадлежит этот файл. В каждой папке может быть только один пакет, и каждый файл .go должен объявлять одно и то же имя пакета в начале своего файла. В этом примере код принадлежит основному пакету. <br/>
Причем главный пакет программы должен называться `main`. Так как именно данный пакет определяет, что будет создаваться исполняемый файл приложения, который после компиляции можно будет запускать на выполнение.

`import` — это ключевое слово Go, которое сообщает компилятору Go, какие другие пакеты будут использованы в этом файле.


## Шаг 3: Запуск программы Go

Для запуска программы выполните команду с указанием названия основного Go файла:

```bash
go run main.go
```

Или с указанием пути к каталогу где расположен основной Go файл:

```bash
go run ./cmd/app
```
