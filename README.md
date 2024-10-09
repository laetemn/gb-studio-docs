# Website

Este site foi criado usando [Docusaurus 2](https://docusaurus.io/), um gerador de sites estáticos moderno.

### Instalação

```
$ yarn
```

### Desenvolvimento local

```
$ yarn start
```

Este comando inicia um servidor de desenvolvimento local e abre uma janela do navegador. A maioria das alterações são refletidas ao vivo sem precisar reiniciar o servidor.

### Construir

```
$ yarn build
```

Este comando gera conteúdo estático no diretório `build` e pode ser disponibilizado usando qualquer serviço de hospedagem de conteúdo estático.

## Localização

### Adicionando um novo local

Adicione sua nova localidade ao `./docusaurus.config.js` adicionando um novo código de país ao array `locales` e adicionando o rótulo de localidade ao `localeConfigs`.

```
  i18n: {
    defaultLocale: "en",
    locales: ["en", "de", "es", "pl"],
    localeConfigs: {
      en: {
        label: "English",
      },
      de: {
        label: "Deutsch",
      },      
```

Crie uma nova pasta para os arquivos Markdown de localidade

```bash
mkdir -p i18n/LOCALE_CODE/docusaurus-plugin-content-docs/current
# e.g. mkdir -p i18n/de/docusaurus-plugin-content-docs/current
```

Em seguida, copie os arquivos em inglês atuais para o seu idioma

```bash
cp -r docs/* i18n/LOCALE_CODE/docusaurus-plugin-content-docs/current
# e.g. cp -r docs/* i18n/de/docusaurus-plugin-content-docs/current
```

### Atualizando o conteúdo local

Você pode editar os arquivos em `i18n/LOCALE_CODE/docusaurus-plugin-content-docs/current` para atualizar o conteúdo do seu idioma.

Você pode executar o site do seu local localmente usando

```
$ yarn start -- --locale LOCALE_CODE
```

e.g. para executar o site Alemão

```
$ yarn start -- --locale de
```
