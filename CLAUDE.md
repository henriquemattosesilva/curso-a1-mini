# Curso A1 Mini (Bambu Lab A1 Mini + Bambu Studio)

Curso web local e offline para o Henrique aprender a **Bambu Lab A1 Mini** (comprando em out/2026) e o
**Bambu Studio**, com foco nas peças do **Topomural** (hexágono de relevo 124 mm, moldura, gravata de
encaixe, porta-medalhas, ímãs embutidos, cores). Bico 0,4 no início, 0,2 depois; 1 cor sem AMS (BMCU no futuro).
Sucessor do `curso-impressao-3d` (genérico, Ender 3) e do guia `ender-3`.

## Como abrir
Abrir `index.html` no navegador (file://). Arquivo único, sem build, sem dependências externas.

## Estrutura
- Cada módulo é `<section class="mod" id="mN" data-titulo="..." data-grupo="..." data-quiz="N">`.
  Sumário (com grupos), caixa "Concluí" e quiz são gerados pelo script.
- Quizzes: objeto `Q` (chave = `data-quiz`), formato `[pergunta, [opções], índiceCerto, explicação]`.
- Simuladores: anatomia clicável (m1, `PARTES`), volumétrica (m9, `calcVol`), costura no hexágono
  (m13, `desenhaSeam`), escadinha do relevo + altura variável (m15, `desenhaRelevo`), camada da pausa do
  ímã (m16, `desenhaIma`), cores por altitude (m17, `desenhaFaixas`). Terreno comum: funções `g`/`H`/`camadas`.
- Diagnóstico (m22): array `DEF` = `[título, palavras-chave, [causas]]`.
- localStorage (try/catch): `cursoA1Mini_v1` (progresso), `cursoA1MiniTema`, `cursoA1MiniCheck`.

## Módulos (24)
0 Como usar · 1 Partes · 2 O que comprar · 3 Instalação · 4 Filamento · 5 Tour Bambu Studio ·
6 Ferramentas da placa · 7 Qualidade · 8 Força · 9 Velocidade · 10 Suporte · 11 Outros/Multimaterial ·
12 Perfis filamento/impressora · 13 Costuras · 14 Tempo×força×beleza · 15 Receitas Topomural ·
16 Ímã embutido (pausa) · 17 Cores com 1 carretel · 18 Bico 0,2 / troca de hotend · 19 Calibração ·
20 Manutenção · 21 Entupimento/HMS · 22 Diagnóstico · 23 Checklist/glossário

## Decisões
- Nomes dos ajustes em **inglês** (a tradução PT do Bambu Studio muda por versão) + explicação em PT.
- Tags: `tag t` Topomural, `tag a` A1 Mini, `tag c` "confira" (detalhe que muda com versão/firmware).
- Folga de encaixe e diâmetro do vão do ímã **moram no gerador**; compensação X-Y do fatiador fica em 0.
- Pausa de ímã = primeira camada em que o vão some; altura variável antes, pausa por último.

## A confirmar quando a máquina chegar (itens marcados "confira")
Nome exato de "Adicionar pausa"/"Trocar filamento" na versão dele; se a pausa afasta a cabeça; trava do
hotend; menus da tela; local do microSD; comportamento de "Change filament" sem AMS; scarf seam na versão.

## Backlog
- Atualizar os itens "confira" com o que ele vir na máquina real (fotos dele).
- Módulo BMCU detalhado quando comprar.
- Diário de impressões (perfil usado × resultado) por peça do Topomural.

## Publicação (05/10/2026)
- Repositório **público** `henriquemattosesilva/curso-a1-mini` (público porque o Pages grátis exige).
- **GitHub Pages:** https://henriquemattosesilva.github.io/curso-a1-mini/ (branch `main`, raiz).
- Para atualizar: editar `index.html`, `git commit` e `git push`. O Pages republica sozinho em ~1 min.
- O progresso/checklist fica no `localStorage` de cada aparelho (celular e PC não compartilham).
