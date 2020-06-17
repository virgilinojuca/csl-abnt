# CSL da ABNT para Zotero
Estilo de citação em Citation Style Language (CSL), atualizado conforme padrões da ABNT de 2018 (NBR 6023:2018 e NBR 10.520:2002), compatível com Zotero.

O estilo é desenvolvido e atualizado por mim mesmo, [@virgilinojuca](https://github.com/virgilinojuca), para uso pessoal, portanto com muitas decisões de gosto próprio. Provavelmente outros encontrarão limitações (mais sobre isso abaixo), mas contribuições são bem vindas.

## Destaques

* __Estilo refeito quase do zero conforme a norma de 2018:__ Não há mais `<>` nos endereços de sites, e termos em latim ("_et al._", "_In_", "_S. l._", "_s. d._"...) estão em itálico.

* __O estilo procura utilizar o máximo possível dos campos estabelecidos pela Citation Style Language__, por mais que [não apareçam claramente disponíveis para preenchimento no Zotero](https://www.zotero.org/support/kb/item_types_and_fields#citing_fields_from_extra), a fim de poder resultar em referências o mais completas e parecidas possíveis com o especificado pela norma.

	* Exemplo: quando o documento é de autoria de algum órgão público, este pode ser colocado no campo `authority`, assim como o ente federativo ou país deve ser colocado no campo de autor mesmo.
	
		Seguindo o __Exemplo 2__ do item __8.1.2.2__ (p. 38) da norma, "Ministério da Justiça" seria inserido como `authority` [utilizando o campo Extra](https://www.zotero.org/support/kb/item_types_and_fields#citing_fields_from_extra), e o autor do documento seria apenas "Brasil".
	
		> BRASIL. Ministério da Justiça. __Relatório de atividades__. Brasília, DF: Ministério da Justiça, 1993. 28 p.

* Diferentemente de outros estilos ABNT disponíveis na internet, URLs de acesso, identificadores (ISBN, ISSN, DOI) e algumas outras informações (como características físicas) aparecerão __sempre__ que informadas, independente do tipo de documento.

* Procuro documentar o máximo possível, para que outros possam também utilizar o estilo :)

## Limitações

Como o estilo é desenvolvido para uso pessoal, tomei decisões baseadas no meu gosto, que pode não agradar a todos os usuários. Além disso, como não trabalho com certos tipos de documentos (por exemplo, legislação), não cheguei a detalhar como eles devam ser exibidos. Outros problemas são originados das limitações da própria Citation Style Language (CSL), podendo ser contornadas com edição manual da bibliografia gerada no Word.

* A mais visível: subtítulos deveriam ficar em peso normal, mas ficam em negrito, pois são inseridos junto com o título. Isso é uma limitação da CSL, que não tem campo próprio para subtítulo ou algum tipo de suporte a regex. Até pensei em configurar o estilo de maneira que algum outro campo fosse usado como subtítulo, como o `title-short`, mas conclui que seria muita gambiarra. Preferi usar o `title-short` para outra coisa (ver limitação seguinte). Nesse caso, após geração da bibliografia no Word, o usuário, se fizer muita questão, deve remover o negrito manualmente de todos os subtítulos.

* Quando não há autor e o título deve ser usado como autor, a primeira palavra do título deve ser digitada manualmente em caixa alta. Essa palavra deve ser repetida no campo `title-short`. __Exemplo 1__ do item __8.1.4__ da norma (p. 39):

	>PEQUENA biblioteca do vinho. São Paulo: Lafonte, 2012.
	
	Neste caso, o título deve ser inserido no Zotero como "PEQUENA biblioteca do vinho" assim mesmo, com a primeira palavra em caixa alta. Para que ele possa receber citações no corpo do texto (PEQUENA..., 2012), a palavra "Pequena" deve ser adicionada como `title-short` [no campo Extra](https://www.zotero.org/support/kb/item_types_and_fields#citing_fields_from_extra).

* No caso de "outras informações" em artigo de jornal/revista, referentes ao artigo, elas teriam que ser adicionadas como parte do título. __Exemplo 6__ do item __7.7.5__ (p. 13) da norma:

	> MENDONÇA, Lenny; SUTTON, Robert. Como obter sucesso na era do código aberto. Entrevistado: Mitchekk Baker. __HSM Management__, São Paulo, ano 12, v. 5, n. 70, p. 102-106, set./out. 2008.
	
	O texto "Entrevistado: Mitchekk Baker" teria que ficar inserido dentro do título.
	
	> __Um comentário__: essa parte é contraditória, pois a norma diz que, no caso de entrevistas, o entrevistado é que deve ser colocado como autor, conforme o item __8.1.1.9__.
	
* Não tem como fazer referência para __parte__ de trabalho acadêmico. Limitação do CSL, mas que talvez até pudesse ser contornada com citações do tipo "capítulo de livro".

* Quando o autor é um município ou estado homônimo, não dá para deixar em caixa baixa a especificação entre parênteses. Ex: "RIO DE JANEIRO (Município)".

*  Até poderia fazer, mas, no caso de patentes, foi decisão minha não mudar o separador de ponto por vírgula entre nome, data de depósito e concessão, quando há URL. Me pareceu mais erro na norma do que outra coisa, por isso mantive o ponto.
