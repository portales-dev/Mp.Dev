# Atividade Aula 03 - CSS
 
## Tema da página
- Tema: Portfólio pessoal (landing page) do desenvolvedor Marcos Portales, com seções de Início, Sobre, Habilidades e Contato.
## Cores escolhidas
- Cor de fundo principal (`--bg: #13131F`): usada no `body`, na `.inicio` e no `.inicio-gif`
- Cor de fundo secundária (`--bg-soft: #171b21`): usada no `.contato-card`
- Cor do texto (`--text: #f4f5f7`): usada no `body`, no `.logo`, na `.nome h1` e no `.sobre`
- Cor de texto mais apagada (`--text-faint: #6b7280`): usada no `.nome b`
- Branco (`--branco: #ffffff` / `#FFF`): usada nos textos dos botões (`.inicio-botao-principal`, `.contato-botao`) e nos textos da seção de contato
- Fundo escuro semitransparente (`#00000031` / `#1f1f1f`): usada no `.contato-conteudo` e nos botões (`.inicio-botao-principal`, `.contato-botao`)
## Seletores utilizados
- Seletor de tag: `*` (reset geral), `html`, `body`, e seletores de tag aninhados como `.logo p`, `.nome h1`, `.nome b`, `.about h2`, `.about p`, `.habilidade-conteudo h2`, `.contato h2`, `.menu-links a`
- Seletor de classe: `.container`, `.topo`, `.logo`, `.menu-links`, `.inicio`, `.inicio-card`, `.inicio-botao`, `.inicio-gif`, `.underline`, `.about`, `.carousel`, `.group`, `.card`, `.habilidade-img`, `.contato-conteudo`, `.contato-tag`, `.contato-card`, `.contato-botao`, `.footer`, entre outras
- Seletor de id: `#linha` (único id efetivamente estilizado no CSS; os demais ids do HTML — `#inicio`, `#sobre`, `#habilidades`, `#contato` — são usados como âncoras de navegação do menu)
## Onde foram aplicados margin, padding e border
- **Margin**: no `*` (reset geral, `margin: 0`), no `.container` (`margin: 0 auto`), no `.underline` e no `.about p` (`margin: 0 auto`, para centralizar), no `.habilidade-img` (`margin: 0 auto 5px`) e nos parágrafos de contato (`.contato-texto p`, `margin-bottom: 15px`)
- **Padding**: no `.container` (`padding: 0 20px`), no `.topo-conteudo`, no `.menu-links`, no `.inicio` (`padding: 150px 0`), nos botões `.inicio-botao` e `.contato-botao`, no `.inicio-gif`, no `.card` (cards da seção de habilidades) e no `.contato-card`
- **Border**: no `.inicio-botao-secundario` (`border: 1px solid var(--card-border)`) e no `.contato-tag` (`border: 1px solid #fff8f8`)
- **Border-radius**: no `.menu-links`, nos botões (`.inicio-botao`, `.contato-botao`), no `.inicio-gif`, no `.underline`, nos `.card` e `.habilidade-img` da seção de habilidades, e no `.contato-card`
## Como o box model foi utilizado
No projeto foi usado `* { margin: 0; padding: 0; box-sizing: border-box; }` no reset geral, garantindo que padding e border sejam incluídos na largura total de todos os elementos, evitando que as caixas "estourem" o layout.
 
No elemento `.card` (cards da seção de Habilidades), o box model funciona assim:
- **Content**: a imagem do ícone da tecnologia (`.habilidade-img`)
- **Padding**: `15px` de espaço interno entre o ícone e a borda do card
- **Border**: definida como `transparent` (a borda existe estruturalmente, mas some visualmente; o destaque do card vem do `box-shadow`)
- **Margin**: o espaçamento entre os cards é feito pelo `gap: 12em` do `.group`, que os separa horizontalmente
## Dificuldade encontrada e como ela foi resolvida
Uma das dificuldades foi que o `.container` estava fixado com `max-width: 1100px`, o que fazia com que os cards da seção de Habilidades ficassem menores do que deveriam, sem ocupar os 95% de largura definidos para o carrossel. Depois de identificar o problema, o valor foi ajustado para `max-width: 95%`, corrigindo o tamanho dos cards.
 
Outra dificuldade foi que, com apenas 5 ícones no `.group` do carrossel, eles "sumiam" antes de a animação completar o ciclo, deixando um espaço vazio na tela. A solução foi aumentar a quantidade de ícones do grupo (de 5 para 7), preenchendo melhor o espaço e evitando que o carrossel ficasse vazio durante a rotação.
 
## Uso de Inteligência Artificial
A IA foi utilizada apenas como ferramenta de apoio, para correção ortográfica e de texto (README e comentários) e para tirar dúvidas pontuais sobre propriedades CSS.