# Conciliador-de-Planilhas-Excel
Aplicação web que concilia notas fiscais entre a planilha do SAP e a do fornecedor usando CNPJ + número da nota como chave. Confere campo a campo (valores, impostos, datas), aponta divergências e exporta um relatório em Excel. Roda 100% no navegador.

# ConciliaSAP

Ferramenta web para conciliar notas fiscais entre a planilha do SAP (o que foi lançado) e a planilha do fornecedor.

## Como funciona
- **Chave composta:** cada nota é identificada pelo CNPJ + número da nota. CNPJ com ou sem pontuação e números com zeros à esquerda são normalizados automaticamente.
- **Conferência campo a campo:** nas notas presentes nas duas planilhas, compara os campos escolhidos (valor total, ICMS, IPI, datas etc.), com tolerância configurável para centavos.
- **Notas desconsideradas:** notas que estão em só uma das planilhas são listadas à parte e não entram no relatório.
- **Exportação Excel:** gera um relatório com as notas conciliadas, indicando se cada uma está OK ou com erro e quais campos divergiram.

## Como usar
Abra o `ConciliaSAP.html` no navegador, importe as duas planilhas (.xlsx, .xls ou .csv), escolha as colunas e execute a conciliação. Os dados são processados localmente no navegador e não são enviados para nenhum servidor.

**Tecnologias:** HTML, JavaScript, Tailwind CSS, SheetJS.
