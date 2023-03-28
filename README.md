# mavka-npm-setup

Цей репозиторій містить приклад конфігурації [Мавки](https://xn--80aaf6ah.xn--j1amh/) для використання зі скриптами пакетного менеджера NPM.

Також можна налаштувати конфігурацію, використовуючи завдання VS Code, як це зробити
можна переглянути [ось тут](https://github.com/dkostmii/mavka-vs-code-setup).

## Як створити новий проект

> **Note**
> Для цього необхідно встановити NodeJS та пакетний менеджер NPM.
>
> **Note**
> Аби мати можливість запустити готовий проект, зроблений за цим принципом,
> необхідно виконати команду `npm install`.
>
> Виконання цієї команди встановить усі залежності, перелічені у [`package.json`](./package.json),
> у тому числі Мавку.

1. Ініціалізація

    ```bash
    npm init -y
    ```

2. Встановлення Мавки, як `devDependency`

    ```bash
    npm i -D mavka
    ```

3. У файлі [`package.json`](./package.json) замінити:

    ```json
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1"
    },
    ```

    на

    ```json
    "scripts": {
      "start": "мавка старт"
    },
    ```

4. Створити файл [`.gitignore`](./.gitignore) із вмістом:

    ```text
    node_modules/
    ```

## Запуск проєкту

Переконайтесь, що ви встановили залежності за допомогою:

```bash
npm install
```

Запустіть NPM скрипт `start` за допомогою команди:

```bash
npm run start
```

або за допомогою вкладки **NPM Scripts** VS Code

![Запуск NPM скрипта у VS Code](./img/vs-code-npm-scripts.png)
