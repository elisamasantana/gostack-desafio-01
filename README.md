# gostack-desafio-01
Aplicação para armazenar repositórios de um portfólio, que possibilita a criação, listagem, atualização e remoção dos repositórios (permite também que os mesmos possam receber 'likes').

<article class="markdown-body entry-content" itemprop="text"><p><a target="_blank" rel="noopener noreferrer" href="https://camo.githubusercontent.com/d25397e9df01fe7882dcc1cbc96bdf052ffd7d0c/68747470733a2f2f73746f726167652e676f6f676c65617069732e636f6d2f676f6c64656e2d77696e642f626f6f7463616d702d676f737461636b2f6865616465722d6465736166696f732e706e67"> </a></p>

 
<h2><a id="user-content-rocket-sobre-o-desafio" class="anchor" aria-hidden="true" href="#rocket-sobre-o-desafio"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><g-emoji class="g-emoji" alias="rocket" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f680.png">🚀</g-emoji> Objetivo: </h2>
<p>Aplicar conhecimentos sobre métodos de requisição/rotas aprendidas na aula de Node.js na GoStack da RocketSeat. Estes métodos são:</p> 
<p>- POST : Lista os dados criados</p>
<p>- POST : Cria os dados</p>
<p>- PUT : Atualiza os dados criados sob parâmetro</p>
<p>- DELETE : Deleta os dados criados sob parâmetro</p>

<p>Esta aplicação descende do template contido no repositório: https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/desafio-conceitos-nodejs.</p>

<p>Esta aplicação contém TDD: Testing Driven Development. Estes testes validam cada rota a fim de confirmar se as rotas estão operando conforme o esperado.
Os requisitos dos testes que estão presentes no README do repositório da rocketseat são:</p>

<ul>
<li>
<p><strong><code>should be able to create a new repository</code></strong>: A aplicação deve permitir que um repositório seja criado, e retorne um json com o projeto criado.</p>
</li>
<li>
<p><strong><code>should be able to list the repositories</code></strong>: A aplicação deve permitir que seja retornado um array com todos os repositórios que foram criados até o momento.</p>
</li>
<li>
<p><strong><code>should be able to update repository</code></strong>: A sua aplicação deve permitir que sejam alterados apenas os campos <code>url</code>, <code>title</code> e <code>techs</code>.</p>
</li>
<li>
<p><strong><code>should not be able to update a repository that does not exist</code></strong>: Valida-se na rota de update se o id do repositório enviado pela url existe ou não. Caso não exista, retorna um erro com status <code>400</code>.</p>
</li>
<li>
<p><strong><code>should not be able to update repository likes manually</code></strong>: Valida-se na rota de update que não se altere diretamente os likes desse repositório, mantendo o mesmo número de likes que o repositório já possuia antes da atualização. Isso porque o único lugar que deve atualizar essa informação é a rota responsável por aumentar o número de likes.</p>
</li>
<li>
<p><strong><code>should be able to delete the repository</code></strong>: Verifica a permissão para deleção de um projeto, e ao fazer a exclusão, ele retorna uma resposta vazia, com status <code>204</code>.</p>
</li>
<li>
<p><strong><code>should not be able to delete a repository that does not exist</code></strong>: Valida na rota de delete se o id do repositório enviado pela url existe ou não. Caso não exista, retorna um erro com status <code>400</code>.</p>
</li>
<li>
<p><strong><code>should be able to give a like to the repository</code></strong>: A aplicação deve permitir que um repositório com o id informado possa receber likes. O valor de likes deve ser incrementado em 1 a cada requisição, e como resultado, retornar um json contendo o repositório com o número de likes atualizado.</p>
</li>
<li>
<p><strong><code>should not be able to like a repository that does not exist</code></strong>: Valida na rota de like se o id do repositório enviado pela url existe ou não. Caso não exista, retorna um erro com status <code>400</code>.</p>
</li>
</ul>

<h2><a id="user-content-memo-licença" class="anchor" aria-hidden="true" href="#memo-licença"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><g-emoji class="g-emoji" alias="memo" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4dd.png">📝</g-emoji> Licença</h2>
<p>Esse projeto está sob a licença MIT. Veja o arquivo <a href="/Rocketseat/bootcamp-gostack-desafios/blob/master/desafio-conceitos-nodejs/LICENSE">LICENSE</a> para mais detalhes.</p>
<hr>

</article>
