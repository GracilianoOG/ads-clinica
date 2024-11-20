# 💻 Projeto

## 📖 Descrição

Esse projeto faz parte da primeira avaliação do curso de Análise e Desenvolvimento de Sistemas da disciplina de *Ambiente de Edição Web*. A partir de templates fornecidos, foi designado o desenvolvimento de um site para uma clínica qualquer utilizando HTML e CSS.

A princípio eu não iria postar o projeto no GitHub, mas foi permitida a entrega pelo mesmo. Isso facilita não apenas a revisão do código, como também é possível utilizar o GitHub Pages para postar o site, o que facilita a vida do professor na hora da verificação 😉

Me desafiei a tornar o site responsivo para dispositivos móveis e implementar um menu *hamburguer* apenas com CSS. Também aproveitei para praticar (e revisar) com funções como `clamp` para tornar o texto um pouco mais flexível. Além disso, consegui entender melhor como funciona o `fit-content` e seus derivados.

Tive alguns desafios, como ter que utilizar seletores mais específicos para fazer o menu mobile funcionar do jeito que eu queria (quebrando o padrão BEM).

As imagens de cabeçalho foram redimensionadas e tratadas com o software de edição de imagens GIMP. Um filtro de blur gaugasiano com 3px foi aplicado para diminuir o destaque da imagem e dar mais atenção ao conteúdo textual do cabeçalho.

## 🎯 Requisitos (AV2)

Montar um código de CSS para modificar o estilo do trabalho de AV1. Além do estilo da página, deve incluir no seu código alguns elementos: 

1. classe de div flexível para telas diferentes
2. classe de div com figura de background fixa
3. uma div com bordas arredondadas
4. trocando a cor do texto de link e retirando o sublinhado

## 🎯 Requisitos (AV1)

Criar um site com os conteúdos abordados até aqui. Os temas principais que deverão ser abordados são:

- Formulários
- Estruturação e formatação de texto
- Mídias
- Tabelas

### Instruções

Você deve criar um site de uma instituição de atendimento ao público

Este site deve conter o seguinte menu de navegação:

- Página Principal
- Sobre o local de atendimento
- Horário de Atendimento
- Contato

**Obs:** Deve, obrigatoriamente, utilizar todos os assuntos abordados nas aulas.

Abaixo itens de como cada página deve ser criada e estruturada.

### Estrutura das Páginas

Todas as páginas terão que seguir um padrão pré-definido.
Utilize o arquivo template.html para utilizar como base.

#### Menu

Deve ficar o Menu Padrão em todas as páginas.
Footer padrão em todas as páginas.

#### Página Principal

Deve ter uma imagem no header
Uma breve descrição da empresa.

#### Sobre o local de atendimento

Deve ter uma imagem diferente no Header
Um texto falando sobre a clínica.

#### Horário de Atendimento

Deve ter uma imagem diferente no header.

Um pequeno texto falando sobre os serviços, e uma tabela de preços, onde cada linha é um serviço, com o preço de cada um de acordo com os dias da semana.

#### Contato

Deve ter uma imagem diferente no Header.

Deve ter:

- Os telefones de contato (celular e whatsapp)
- Endereço completo da clínica
- Um Iframe com o Google Maps apontando o endereço da clínica

Um formulário de contato com:

- Nome (type="text")
- E-mail (type="email")
- Assunto (type="text")
- Mensagem (textarea)
- Botões de envias e limpar formulário

## 🛠️ Ferramentas

- Estruturado com HTML semântico
- Estilizado com CSS
- Estilos gerados com [pré-processador Sass](https://sass-lang.com/)
- Desenvolvimento Mobile-first
- Design Responsivo
- Classes nomeadas seguindo a metodologia [BEM](https://en.bem.info/methodology/quick-start/)

## 📌 Links úteis

- [Imagem do cão - formulário](https://pixabay.com/illustrations/dog-dachshund-puppy-sit-drawing-8165447/)
- [Validação de formulário](https://css-tricks.com/form-validation-ux-html-css/)
- [Links acessíveis](https://www.freecodecamp.org/news/link-accessibility-colors-are-not-enough/)
- [Breakpoints do Bootstrap 5](https://getbootstrap.com/docs/5.0/layout/breakpoints/)
- [Background com múltiplos elementos](https://www.w3schools.com/Css/css3_backgrounds.asp)
- [Variáveis CSS](https://www.w3schools.com/css/css3_variables.asp)
- [Quebra de conteúdo](https://desenvolvimentoparaweb.com/css/css-min-content-max-content-fit-content/)
- [Favicon utilizado](https://favicon.io/emoji-favicons/cat-face)
- [Problema com z-index](https://www.freecodecamp.org/news/4-reasons-your-z-index-isnt-working-and-how-to-fix-it-coder-coder-6bc05f103e6c/)

## 🗂️ Estrutura do projeto

### Separação dos arquivos

- `src`: arquivos de código fonte do projeto;
- `assets`: arquivos como imagens e ícones essenciais;
- `css`: estilo das páginas;
- `scss`: estilos do pré-processador;
- `pages`: páginas HTML.

### Separação do Sass

- `base`: estilos base para todas as páginas;
- `components`: componentes que podem existir de forma independente (Block elements);
- `layout`: componentes estruturais que ajudam a compor as páginas;
- `pages`: estilos exclusivos de cada página;
- `utils`: estilos, funções e outros arquivos que auxiliam na montagem das páginas.

## 🧱 Template inicial

### HTML: template.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Template - Modelo</title>
    <link rel="stylesheet" href="base.css">
</head>
<body>
    <div class="wrapper">
        <div class="menu">
            <!-- Aqui vai o seu menu -->
            <ul>
                <li><a href="#">Link</a></li>
            </ul>
        </div>

        <div class="main">
            <div class="header">
                Header
                <!-- Aqui vai o seu header -->
            </div>
    
            <div class="content">
                Content
                <!-- Aqui vai o seu conteúdo -->
            </div>
    
            <div class="footer">
                Footer
                <!-- Aqui vai o seu rodapé -->
            </div>
        </div>
    </div>
</body>
</html>
```

### CSS: base.css

```css
html, body {
  margin: 0;
}
body {
  background-color: #f1f1f1;
  display: flex;
  justify-content: center;
}
.wrapper {
  width: 1200px;
  display: flex;
  margin: 0 auto;
  background-color: aquamarine;
}
.main {
  display: flex;
  flex-flow: column;
  width: 85%;
}
.menu {
  width: 15%;
  background-color: aqua;
  padding: 10px 20px 0px;
}
.header {
  background-color: rgb(5, 108, 108);
  min-height: 150px;
}
.content {
  background-color: white;
  min-height: 300px;
  padding: 20px;
}
.footer {
  background-color: rgb(99, 56, 240);
  min-height: 150px;
}
```

## 🧑🏻‍💻 Conclusão

Projeto desenvolvido por Gabriel, aluno do curso de Análise e Desenvolvimento de Sistemas da disciplina de Ambiente de Edição Web ministrada pelo professor Túlio.