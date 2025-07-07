# Cálculos teóricos de coordenadas normais: aspectos computacionais

#### Programas necessários

Os programas necessários para que os cálculos da apresentação sejam reproduzidos podem ser baixados do site do ORCA:

https://orcaforum.kofo.mpg.de/app.php/portal

Após o registro e o login na página você pode ir para a página de "Downloads" onde será possível baixar a versão 4.2.1 do ORCA e a versão
do Avogadro otimizada para o Orca.

Mais detalhes em relação aos programas podem ser encontrados nos seguintes sites: <br />

1-https://www.faccts.de/customer/login?came_from=/customer <br />
2-https://www.faccts.de/docs/orca/6.0/tutorials/index.html<br />
3-https://avogadro.cc/docs/getting-started/introduction/ <br />

Dentre os arquivos do tutorial estão:

1-Cálculo do espectro da Acetona <br />
2-Cálculo do espectro do Ácido Acético <br />
3-Cálculo do espectro da Água "linear" e com a geometria otimizada (H2O_geom) e com diferentes métodos (H2O_compara_metodo) <br />
4-Cálculo do espectro da uracila cátion, neutra e ânion, em vácuo e em água (CPCM) <br />

Estes cálculos foram feitos utilizando um computador com o sistema operacional Windows 11, executando os cálculos do PowerShell.
Antes de visualizar os resultados dos cálculos, para a versão 4.2.1 do ORCA é necessário converter o output do cálculo usando o seguinte comando:

gc #ARQUIVO_DE_OUTPUT | out-file -encoding #ARQUIVO_DE_OUTPUT_CONVERTIDO
 
Sendo que #ARQUIVO_DE_OUPUT e #ARQUIVO_DE_OUTPUT_CONVERTIDO devem ser substituidos pelo nome dos arquivos gerados na execução do seu cálculo.

Após um cálculo de frequências, as coordenadas normais podem ser extraídas executando os seguinte comando:

orca_pltvib.exe #ARQUIVO.hess all

Sendo que #ARQUIVO.hess é a hessiana calculada pelo ORCA a partir do seu arquivo de input. O argumento "all", indica que todos os modos vibracionais
gerados devem ser extraídos. Se o arquivo de output e as coordenadas normais extraídas do arquivo .hess estiverem na mesma pasta, os modos normais
podem ser protamente visualizados assim que o arquivo de output seja aberto no Avogadro.


#### Copyright

Copyright (c) 2025, Vitor Paschoal
