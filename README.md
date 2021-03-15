# Teste Técnico Desenvolvedor(a) Frontend Júnior [REMOTO]

Neste repositório você encontra o enunciado do teste técnico para a vaga de Desenvolvedor(a) Frontend Júnior [REMOTO] da [Instruct](https://instruct.com.br/)!
Você provavelmente chegou aqui através da indicação de alguma pessoa da empresa após passar pelas [outras etapas](https://instruct.com.br/trabalhe-com-a-gente/processo-de-selecao/) do processo seletivo. Se este não for o seu caso e mesmo assim você implementar alguma solução para este exercício, ele não será avaliado.

> Você pode usar o problema descrito aqui para exercitar suas habilidades de desenvolvimento, mas a sua solução será avaliada por alguém da Instruct apenas se você estiver no processo seletivo da vaga de Desenvolvedor(a) Frontend Júnior [REMOTO].

Caso tenha interesse em se candidatar para uma vaga da Instruct, siga as instruções no site: https://instruct.com.br/trabalhe-com-a-gente/

Nessa página você encontra as vagas abertas atualmente e todos os detalhes de nosso processo seletivo. Se você não encontrou uma vaga que pareça adequada, confira a página novamente em um ou dois meses, ela é atualizada com certa frequência.

## Problema

A Vough é uma empresa de marketing que vem buscando novas oportunidades de negócio, porém o time comercial não possui nenhuma ferramenta que facilite a visualização de clientes em potencial.

## Solução

Para ajudar o time comercial, você deve desenvolver uma interface que liste os contatos de clientes em potencial (leads). A tela deve fornecer informações úteis que facilitem a comunicação entre o time comercial e o cliente e sua empresa. 

A lista de contatos deve ser consumida via API REST [encontrada aqui](https://jsonplaceholder.typicode.com/users), para facilitar a usabilidade dois filtros devem ser disponibilizados: por nome do contato (campo `name`) e pelas possíveis categorias das empresas (encontradas no campo `company.bs`).

**Exemplo:** `aggregate real-time technologies`: Aqui possuimos 3 categorias, nossa aplicação deve permitir que elas sejam filtradas separadamente.

Como o time comercial nem sempre está nos escritórios da Vough, a interface deve ser responsiva para que seja facilmente acessível via smartphones e deve seguir a referência visual encontrada neste repositório como logo, fontes e cores marcas registradas da empresa **sem a utilização de frameworks visuais prontos como Bootstrap, Tailwind entre outros**.

O projeto deve ser desenvolvido com base na estrutura encontrada neste repositório utilizando [Nuxt.js](https://nuxtjs.org/) e publicado no [Heroku](https://www.heroku.com/) utilizando Free Tiers disponíveis.

## Recomendações

 - Utilize apenas [CSS/SCSS](https://sass-guidelin.es/) desenvolvido por você.
 - Utilize HTML semântico.
 - Se preocupe com a UX e UI do projeto elas serão levadas em consideração na avaliação.
 - Utilize Git com boas mensagens de commit.
 - Se atente nas [boas práticas do Vue.js](https://vuejs.org/v2/style-guide/).
 - Para desenvolver utilize o comando `npm run dev` (Se preferir utilize o Yarn).

## Avaliação

Quando você finalizar a implementação, adicione o usuário com o e-mail jobs@instruct.com.br como colaborador do app publicado no Heroku até o fim do prazo estipulado. A partir disso, conseguimos o endereço em que sua app está publicada e seguimos com as validações necessárias.
