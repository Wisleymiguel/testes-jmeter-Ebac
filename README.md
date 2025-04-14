
# 🧪 Testes de Performance com Apache JMeter

Este repositório contém um projeto de testes de performance realizado com o **Apache JMeter**, como parte do curso da EBAC.

---

## 📂 Estrutura do Projeto

```
📁 Testes Apache/
├── Teste ebac.jmx                  # Plano de testes JMeter
├── termos.csv                     # Massa de dados para CSV Data Set Config
├── plugins-manager.jar           # Gerenciador de plugins JMeter
├── /bin                          # Scripts de execução do JMeter
├── /lib/ext                      # Local onde o plugin foi adicionado
```

---

## 🚀 Ferramentas Utilizadas

- **Apache JMeter 5.6.3**  
- **PerfMon Server Agent (Opcional para métricas do servidor)**
- **Plugin Manager (plugins-manager.jar)**
- **VS Code**  
- **Git + GitHub**  
- **Postman (para testes manuais prévios)**  
- **Sauce Labs (para testes em nuvem com Appium)**  
- **Appium + WebDriverIO (caso tenha integrado com mobile)**

---

## 🧩 Plugins Instalados

Instalados via `plugins-manager.jar`:

- **PerfMon (Server Performance Monitoring)**
- **Custom Thread Groups**
- **JSON Formatter (se necessário)**

---

## ⚙️ Como Executar os Testes

### 1. Baixar e Instalar o JMeter

```bash
https://jmeter.apache.org/download_jmeter.cgi
```

### 2. Adicionar o Plugin Manager

- Baixe de: [https://jmeter-plugins.org/install/Install/](https://jmeter-plugins.org/install/Install/)
- Coloque o arquivo `plugins-manager.jar` em:

```
apache-jmeter-5.6.3/lib/ext/
```

Reinicie o JMeter.

---

### 3. Executar o Plano de Testes

- Abra o JMeter
- Vá em `File > Open > Teste ebac.jmx`
- Clique em ▶️ para executar

---

### 4. Relatórios

- O projeto contém os seguintes listeners:
  - View Results Tree
  - View Results in Table
  - Summary Report
  - jp@gc - Active Threads Over Time (gráfico)

---

## ☁️ Integração com Sauce Labs (Mobile Testing)

Se aplicável, este projeto também foi testado em nuvem com o Sauce Labs usando:

```js
'platformName': 'Android',
'deviceName': 'Google Pixel 5',
'platformVersion': '14',
'app': 'storage:filename=ebacshop.aab',
```

---

## 💬 Observações

- Algumas palavras como `carros` e `ebac` funcionam nas requisições, enquanto `frutas`, `jogos` e `art` resultam em erro por causa de **caracteres inválidos na URL**.
- Recomendado usar encoding de URL ou verificar se o domínio permite chamadas GET com determinados termos.

---

## 👨‍💻 Autor

**Wisley Miguel**  
[GitHub](https://github.com/Wisleymiguel)
