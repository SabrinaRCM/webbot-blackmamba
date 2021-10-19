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

```
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('arq1.csv', sep=';')

plt.plot(df['Hora'], df['Valor_total'])
plt.show()
```
```
import pandas as pd
      
dt = pd.read_csv('arq1.csv')

dt.columns
print(dt.valor_total)
```

* Front-End

### Aprendizados Efetivos
