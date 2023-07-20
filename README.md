# Flutter Version Management - FVM
Instalação e configuração do FVM para gerenciamento de versões Flutter

## Pub package
Instalação via pub package (https://fvm.app/docs/getting_started/installation).

1. Executar no `powershell` o comando.
```powershell
dart pub global activate fvm
```
2. Adicionar ao `Path` o caminho dos executáveis.
> Warning: Pub installs executables into 'C:\Users\ddamasceno\AppData\Local\Pub\Cache\bin', which is not on your path.
You can fix that by adding that directory to your system s 'Path' environment variable. A web search for 'configure windows path' will show you how.

```
C:\Users\ddamasceno\AppData\Local\Pub\Cache\bin
```

## Configuração do Repositório
1. Obtendo as configurações.
```
fvm config
```
2. Configuração o apontamento de cache do `Flutter`.
```
fvm config --cache-path c:\fvm
```

## Utilização
Comandos de utilização
1. Use
```
fvm use [version]
```
2. Install
```
fvm install [version]
```
3. Remove
```
fvm remove [version]
```
4. List
```
fvm list
```
5. Releases
```
fvm releases
```
5. Doctor
```
fvm doctor
```

## Configuração do Projeto
1. Setando a versão do `Flutter` para o projeto. No diretório do projeto rodar o comando. 
```
fvm use (version)
```
2. Configuração do vscode.
> - Criar pasta `.vscode` no projeto.
> - Dentro da pasta `.vscode`, criar o arquivo `settings.json`.
3. Colar o contéudo do código abaixo de configuração (https://fvm.app/docs/getting_started/configuration).
```json
{
  "dart.flutterSdkPath": ".fvm/flutter_sdk",
  // Remove .fvm files from search
  "search.exclude": {
    "**/.fvm": true
  },
  // Remove from file watching
  "files.watcherExclude": {
    "**/.fvm": true
  }
}
```
4. Adicionar no `.gitignore` a pasta abaixo.
```
.fvm/flutter_sdk
```
