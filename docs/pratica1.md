# Reflexão Final — Prática 1

1. **Onde está o dado bruto neste projeto?**
   - Tá em `data/raw/`, no arquivo `orders_2026_03_23.csv`. 
   
2. **Qual é o papel do script Python no fluxo?**
   - Ele basicamente lê o CSV, joga os dados no DuckDB e já faz uma consulta pra mostrar um resumo por status.

3. **O que aconteceria se uma coluna do CSV mudasse de nome?**
   - O script ia quebrar porque ele espera os nomes certinhos das colunas. Teria que ajustar o código pra funcionar de novo.

4. **Por que o primeiro commit no Git é importante?**
   - Além de começar o projeto, é ele que começa a versionar tudo. Assim dá pra saber o que mudou, voltar atrás se precisar e pelo que entendo, quando se fala de DataOps, isso é obrigatório pra não perder o controle do pipeline e garantir que todo mundo tá na mesma página, além de rastrear a responsabilidade quem fez as mudanças.

5. **O pipeline funciona, mas ele já pode ser considerado confiável para produção?**
   - Ainda não, falta muita coisa tipo validação, teste, rastreabilidade, etc. Por enquanto é só algo inicial mesmo, só pra mostrar funcionando.
