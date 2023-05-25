# Extração de problems usando get.problems

Extrair grandes quantias de problems via API, visto que a aplicação WEB ira retornar timeout quando o resultado for muito extenso.

- Acesso via Postman

![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/postman.png)

- Exemplo
~~~json
    {
  "jsonrpc": "2.0",
  "params": {
    "output": "extend",
    "recent": "true",
    "selectAcknowledges": "extend",
    "selectTags": "extend",
    "selectSuppressionData": "extend",
    "time_from": "1672684776",
    "source": 3,
    "object": 4
  },
  "method": "problem.get",
  "auth": "xxxxxxxxxxxxxxx",
  "id": 1
}
~~~
**Observação**: auth corresponde ao usuário utilizado no Zabbix destino.

- Passo a passo

1. Consultar a documentação e adequar a query de acordo com suas necessidades.
https://www.zabbix.com/documentation/5.0/en/manual/api/reference/problem/get

2. Após montar a query, efetuar a consulta GET para a API (body)

3. Exportar o json e abri-lo no excel (Importar>JSON)
![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/step3.png)<br>

4. Clicar em Result > List, em seguida PARA A TABELA > OK
![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/step4.png)<br>
![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/step4.1.png)<br>


5. Expandir colunas, fechar e carregar.
![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/step5.png)<br>
![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/step5.1.png)<br>
![](https://github.com/MikeFortes/ZBX_QuerysAPI/blob/main/Code/get.problems/step5.2.png)<br>

6. Pronto