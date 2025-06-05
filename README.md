# Safety Stock Calculation

Este projeto é um script Python que calcula o Estoque de Segurança Ideal (Safety Stock) com base em dados de consumo, estoque atual e preço de transferência, utilizando uma abordagem estatística para estimar a variabilidade da demanda e o tempo de entrega.

## Funcionalidades

- Leitura de arquivos Excel com dados de consumo, estoque atual e preço.
- Cálculo do consumo médio mensal e desvio padrão estimado.
- Identificação automática da coluna de tempo de trânsito (PDT).
- Cálculo do Safety Stock Ideal usando o nível de serviço de 95%.
- Comparação entre o estoque de segurança atual e o ideal.
- Geração de arquivo Excel com resultados, formatação e gráfico comparativo.
- Interface gráfica simples para seleção de arquivos de entrada e saída.

## Requisitos

- Python 3.x
- pandas
- openpyxl
- tkinter (já incluso na maioria das distribuições Python)

## Como usar

1. Execute o script `safety_stock.py`.
2. Selecione o arquivo Excel com os dados de entrada.
3. Escolha onde salvar o arquivo Excel com os resultados.
4. Verifique o arquivo gerado, que contém as planilhas de cálculo e um gráfico comparativo.

## Explicação do cálculo

O cálculo do Safety Stock ideal segue os passos:

- Consumo médio mensal = Consumo total em 24 meses / 24
- Estimativa do desvio padrão = 20% do consumo médio mensal
- Tempo de trânsito (lead time) convertido de dias para meses
- Fator de nível de serviço Z = 1.64 para 95%
- Safety Stock = Z × desvio padrão × √(tempo de trânsito em meses)

---

## Autor

KarolineVollet

---

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.
