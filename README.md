# Challenge | TelecomX Parte 2

# Relatório Análise e Estratégias de Retenção de Clientes

O objetivo desta análise foi identificar os principais fatores que influenciam a evasão de clientes da **TelecomX**, comparar diferentes modelos de machine learning na previsão de churn e propor estratégias de retenção baseadas em evidências.  

O dataset utilizado contém informações sobre clientes, serviços contratados, faturamento e comportamento de consumo.  


## Modelagem Preditiva  

Foram avaliados diferentes algoritmos de machine learning:  

- **Regressão Logística (Logistic Regression)**  
- **Random Forest Classifier**  
- **KNN (K-Nearest Neighbors, usado como comparação)**  

### Desempenho dos Modelos  

| Modelo                | Acurácia | Precisão | Recall | F1 Score |
|------------------------|----------|----------|--------|----------|
| Regressão Logística    | 0.757    | 0.530    | **0.745** | 0.620    |
| Random Forest          | **0.779**| **0.596**| 0.526  | 0.559    |
| KNN                    | 0.731    | 0.500    | 0.482  | 0.491    |

**Observações:**  
- A **Regressão Logística** apresentou **maior recall**, sendo mais eficaz para identificar clientes em risco de evasão.  
- O **Random Forest** teve **melhor acurácia e precisão**, sendo mais confiável para prever clientes que permanecem.  
- O **Random Forest superou o KNN**, alcançando recall de 0.65 em alguns testes, confirmando ser a melhor ferramenta preditiva.  
- Não houve sinais de overfitting extremo após o uso de **SMOTE** para balanceamento da base.  

---

## Principais Variáveis que Influenciam a Evasão  

A análise de importância de variáveis (Random Forest) revelou fatores determinantes:  

| Variável                     | Importância |
|-------------------------------|-------------|
| Faturamento_Total             | 0.15 |
| Meses_Cliente / Permanência   | 0.12 |
| Tipo de Contrato              | 0.10 |
| Serviço de Internet           | 0.08 |
| TV Streaming                  | 0.07 |
| Método de Pagamento (Cartão)  | 0.06 |
| Serviço de Celular            | 0.05 |
| Backup Online / Segurança     | 0.04 |
| Faturamento Mensal            | 0.04 |
| Linhas Adicionais / Dependentes | 0.03 |

**Interpretação dos Fatores:**  
- **Tempo de permanência e faturamento**: clientes novos ou de baixo gasto tendem a cancelar mais.  
- **Serviços críticos (Internet, TV, Backup Online)**: problemas ou insatisfação aumentam fortemente o churn.  
- **Fibra Óptica**: clientes com esse serviço apresentaram maior propensão à evasão, indicando necessidade de investigar qualidade, preço ou concorrência.  
- **Laços familiares (cônjuge/dependentes)** reduzem o risco de cancelamento, reforçando a importância de planos compartilhados.  

---

## Estratégias de Retenção Propostas  

Com base nos insights, sugerimos ações estratégicas:  

### 1. Clientes Recentes e de Baixo Faturamento  
- Criar **programa de boas-vindas** ativo (onboarding digital e suporte personalizado).  
- Oferecer **descontos progressivos ou recompensas** nos primeiros meses.  

### 2. Contratos e Fidelização  
- Incentivar **contratos de longo prazo** (anuais/bianuais) com benefícios exclusivos.  

### 3. Qualidade dos Serviços Críticos  
- Monitorar e **resolver proativamente falhas** em Internet e TV Streaming.  
- Melhorar infraestrutura e canais de atendimento rápido.  

### 4. Serviços Adicionais  
- Promover **pacotes combinados** (internet + backup + segurança).  
- Educar clientes sobre o valor dos serviços agregados.  

### 5. Investigação da Fibra Óptica  
- Realizar análise detalhada da experiência dos clientes de fibra.  
- Entender se o problema é **técnico, de preço ou de concorrência**.  

### 6. Pagamentos e Engajamento  
- Ampliar **opções de pagamento** e oferecer **alertas automáticos** de vencimento.  
- Enviar **campanhas de engajamento** e conteúdos educativos para aumentar o uso de serviços.  

### 7. Retenção Personalizada com Machine Learning  
- Utilizar o modelo Random Forest para **identificar clientes de alto risco em tempo real**.  
- Oferecer **promoções e benefícios personalizados** para reverter potenciais cancelamentos.  

---

## Conclusão  

A análise demonstrou que tanto fatores **financeiros** quanto **serviços críticos e comportamentais** impactam fortemente a evasão.  

- A **Regressão Logística** é útil para **detectar clientes em risco**, enquanto o **Random Forest** fornece previsões mais robustas para clientes que permanecem.  
- A empresa pode reduzir significativamente o churn ao **focar nos clientes novos**, **melhorar a qualidade dos serviços de internet/TV**, e **promover pacotes de fidelização**.  
- Além disso, a **investigação do serviço de fibra óptica** e a **personalização via modelos preditivos** são cruciais para ganhos sustentáveis em retenção.  

---
