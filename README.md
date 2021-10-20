# webbot-blackmamba

### Resumo do Projeto
O projeto foi o desenvolvimento de um Web bot que envia através do telegram informações de ações da bolsa de valores de uma empresa escolhida pelo usuário. As informações incluem histórico da ação através de gráficos.

### Tecnologias adotadas na solução
* Python 3.7 - Linguagem principal;
* Zen of Python - boas práticas para o Projeto;
* PyCharm e/ou Visual Studio Code - IDE's;
* Django, Javascript, HTML5, CSS,  Bootstrap - Front End WEB;
* MySQL - Banco de Dados;
* Conceitos do SCRUM - Norteador do Projeto.
* Principais Bibliotecas Python:  
    **PyMySQL** - interação com nosso Banco de Dados;  
    **Selenium** - navegação pela Web através do WebDriver do Google Chrome;  
    **Beautiful Soup** - interação com o html dos sites para permitir as raspagens de dados;  
    **Pandas / Matplotlib** - ferramentas para gerar e plotar graficos;  
    **Email / Telegram-bot** - envio de alertas e notificações;

### Contribuições individuais/pessoais
* Bibliotecas do Python: Pandas e Matplotlib
> Esse código trata da importação da biblioteca Pandas para que seja feita a leitura do nosso arquivo .csv
##### text.py 
```python
import pandas as pd
# Realiza a leitura do arquivo csv     
dt = pd.read_csv('arq1.csv')

# Define que será feito a leitura das colunas do arquivo
dt.columns
# Exibe na tela a coluna selecionada
print(dt.valor_total)
```
> Esse código integra a biblioteca Pandas que está realizando a leitura do arquivo com a Matplotlib que está criando o gráfico para o usuário
##### graficos.py
```python
import pandas as pd
import matplotlib.pyplot as plt

# Realiza a leitura do arquivo csv
df = pd.read_csv('arq1.csv', sep=';')

# Usa a biblioteca Matplotlib para montar o gráfico e mostrar na tela para o usuário
plt.plot(df['Hora'], df['Valor_total'])
plt.show()
```

* Front-End
> Foi iniciado a montagem de um front end usando HTML, CSS e JS
##### index.html
```html
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>MB Bot</title>
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1,  shrink-to-fit=no"
    />
    <link
      rel="stylesheet"
      href="https://use.fontawesome.com/releases/v5.8.1/css/all.css"
      integrity="sha384-50oBUHEmvpQ+1lW4y57PTFmhCaXp0ML5d60M1M7uH2+nqUivzIebhndOJK28anvf"
      crossorigin="anonymous"
    />
    <link
      href="https://fonts.googleapis.com/css?family=Dosis&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="../css/bootstrap.min.css" type="text/css" />
    <link rel="stylesheet" type="text/css" media="screen" href="style.css" />
  </head>
  <body>
    <div
      class="fixed-top banner"
      style="height: 23%; background-color: rgb(54, 54, 54);"
    >
      <img src="../img/bmlogo.png" class="px-4" alt="Logo BlackMamba" />
      <div
        class="card p-3 bg-transparent float-right text-white border-0"
        style="width: 40%;"
      >
        <form class="row">
          <div class="form-group col-sm-6">
            <label for="exampleDropdownFormEmail2">Endereço de email</label>
            <input
              type="email"
              class="form-control"
              id="exampleDropdownFormEmail2"
              placeholder="email@exemplo.com"
            />
          </div>
          <div class="form-group col-sm-6">
            <label for="exampleDropdownFormPassword2">Senha</label>
            <input
              type="password"
              class="form-control"
              id="exampleDropdownFormPassword2"
              placeholder="Senha"
            />
          </div>
          <div class="form-check ml-3">
            <input
              type="checkbox"
              class="form-check-input"
              id="dropdownCheck2"
            />
            <label class="form-check-label" for="dropdownCheck2">
              Lembrar de mim
            </label>
          </div>
          <button
            type="submit"
            class="btn btn-primary float-right bg-primary col-sm-3"
            style="margin-left: 70%"
          >
            Entrar
          </button>
        </form>
      </div>
      <div class="card bg-transparent border-0 align-right">
        <form>
          <h1>Cadastre - se</h1>
          <div class="row">
            <div class="col">
              <input type="text" class="form-control" placeholder="Nome" />
            </div>
            <div class="col">
              <input type="text" class="form-control" placeholder="Sobrenome" />
            </div>
          </div>
          <div class="form-group mt-2">
            <input
              type="email"
              class="form-control"
              id="exampleDropdownFormEmail2"
              placeholder="email@exemplo.com"
            />
          </div>
          <div class="form-group">
            <input
              type="password"
              class="form-control"
              id="exampleDropdownFormPassword2"
              placeholder="Senha"
            />
          </div>
          <div>
            <a
              role="button"
              class="btn btn-primary bg-primary p-2"
              href="cadastro.html"
              style="width: 100%;"
            >
              Cadastrar
            </a>
          </div>
        </form>
      </div>
    </div>
    <div class="fixed-bottom banner" style="height: 5%;">
      <span class="text-white fixed-bottom"
        >&copy Copyrights reserved by BlackMamba 2019</span
      >
    </div>
    <script src="../js/jquery-3.4.1.min.js"></script>
    <script src="../js/popper.min.js"></script>
    <script src="../js/bootstrap.min.js"></script>
    <script src="../js/main.js"></script>
  </body>
</html>
```

### Aprendizados Efetivos
