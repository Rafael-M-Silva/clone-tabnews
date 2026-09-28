# Clone TabNews — estudo de Next.js

Repositório de estudo inspirado no TabNews, com uma página inicial simples e uma rota de status para praticar a estrutura de um projeto Next.js.

**Projeto desenvolvido para fins educacionais.** Não é uma implementação completa do TabNews.

**Demonstração informada no repositório:** [clone-tabnews-dun-delta.vercel.app](https://clone-tabnews-dun-delta.vercel.app)

## Estado atual

- Página inicial em <code>pages/index.js</code> com link para Bigode Ensina.
- Rota <code>GET /api/v1/status</code> que retorna uma resposta JSON de exemplo.
- Estrutura inicial para teste de integração.
- Arquivo Compose para um PostgreSQL local, ainda sem integração com a rota ou a página.

## Tecnologias e estrutura

Next.js 13, React 18, JavaScript, Jest, Prettier e Docker Compose para o banco local opcional.

~~~text
pages/index.js                  página inicial
pages/api/v1/status/index.js    rota de status
tests/integration/              teste da rota
infra/compose.yaml              banco local opcional
package.json
~~~

## Como executar

Use uma versão de Node.js compatível com <code>.nvmrc</code> e npm:

~~~bash
git clone https://github.com/Rafael-M-Silva/clone-tabnews.git
cd clone-tabnews
npm ci
npm run dev
~~~

Abra [http://localhost:3000](http://localhost:3000) ou acesse <code>http://localhost:3000/api/v1/status</code>. O banco do Compose não é necessário para essas duas páginas.

## Pontos a revisar

O teste de integração usa uma URL local malformada e pode falhar até que ela seja corrigida. O arquivo <code>infra/compose.yaml</code> traz uma senha de banco para desenvolvimento versionada: revise o arquivo e confirme que essa senha não é reutilizada fora do ambiente local. Nenhum valor de credencial é reproduzido aqui.

## Autor

**Rafael Mauricio (Bigode)** · [GitHub](https://github.com/Rafael-M-Silva) · [LinkedIn](https://linkedin.com/in/rafael-mauricio-dev/) · [Bigode Ensina](https://bigodeensina.com.br/)
