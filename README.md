# performanceAgiJmeter

# Teste de Performance - BlazeDemo com JMeter  

Este repositório contém um **teste de performance** utilizando **Apache JMeter** para avaliar o desempenho do site [BlazeDemo](https://www.blazedemo.com).  

## Objetivo  

Testar a performance da aplicação simulando **250 requisições por segundo** e garantir que o **tempo de resposta 90th percentil seja inferior a 2 segundos**.

---

## Cenário de Teste  

### **Compra de Passagem Aérea**  

O teste simula a jornada de um usuário no BlazeDemo:  

1. **Acessar a Página Inicial** (`/`)  
2. **Selecionar um voo** (`/reserve.php`)  
3. **Finalizar a compra** (`/purchase.php`)  
4. **Confirmar a compra** (`/confirmation.php`)  

---

## **Critérios de Aceitação**  

- ** Vazão esperada:** **250 requisições por segundo (RPS)**  
- ** Tempo de resposta (90th percentil):** **Menos de 2 segundos**  
- ** Erros abaixo de 1%**  

---

## **Configuração do JMeter**  

- **Número de Usuários (Threads):** 250  
- **Tempo de Inicialização (Ramp-up):** 1 segundo  
- **Número de Repetições:** 10 ciclos  
- **Modo de Execução:** Teste de Carga e Pico  

## **Relatório Gerado**  
 **Relatório CSV:** [resultado_teste.csv](./resultado_teste.csv)  

---

## **Como Executar o Teste**  

### **Pré-requisitos**  
- Instalar o [Apache JMeter](https://jmeter.apache.org/)  

### **Clonar o Repositório**  
```sh
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio

### ** Executar no JMeter (Interface Gráfica) **
Abra o JMeter
Vá em Arquivo > Abrir e selecione testeBlazeAgi.jmx
Clique no botão de Play para rodar o teste
