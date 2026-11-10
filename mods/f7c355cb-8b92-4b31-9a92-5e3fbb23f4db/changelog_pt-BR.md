# Changelog

## 1.0.5 - 2026-11-10 - Carga antes da tela inicial

**Correções**
- A tela de abertura (o logo antes do menu) agora espera o Split terminar de carregar. Em celulares mais lentos a tela inicial abria com o mod ainda pela metade, e quem entrava num mundo nessa hora ficava sem os itens, blocos e NPCs do mod. A abertura pode demorar mais do que antes: é o tempo de que o mod precisa.
- Se mesmo assim alguém entrar num mundo antes de o mod terminar de carregar, aparece um aviso em vermelho no jogo: saia sem salvar e entre de novo, para não perder os itens do mod.

## 1.0.4 - 2026-11-09 - Revisão das armas

Uma revisão de todas as armas (e do resto do mod) contra as funções que o Terraria do celular realmente tem.

**Correções**
- Sons que não tocavam: a explosão dos mísseis da Bola de Carne, os cliques do álbum de fotos e os potes de Basaltita quebrando (que também não soltavam poeira nem pedaços).
- Paraffin: o rastro do corpo (girando, correndo e na tosse final) dava erro.
- Starshroom: a sentinela extra não era criada.
- Celular Espacial: as informações (relógio, bússola, profundidade e as outras) não funcionavam.
- Muda de Frostbite dava erro ao tentar crescer.
- Boss Checklist: os itens de invocação apareciam sem a cor da raridade.
- O Mágico dava erro ao ir embora no fim do dia (e, no multiplayer, a saída dele não chegava aos outros jogadores).
- O clarão do tiro do Dazzler não seguia a transparência do próprio tiro.
- Ajuste preventivo em chamadas que passavam argumentos a mais do que o celular espera: o fim da munição das armas de longo alcance (Glândula de Balão, Lava Blaster, Heartmelter, Tempestade Estelar, Flamaxe e outras), o Coração de Caranguejo e vários buffs (Metal Pesado, as posturas das armas pesadas, Observador de Estrelas, Vínculo Gelatinoso, os chás, Anel Derretido, Cura Gélida, Fúria Tóxica, Bênção do Piromante, Casa do Mal e debuffs de alguns inimigos).

**Desempenho**
- Dois caches internos se esvaziavam entre um quadro e outro e agora guardam o que deveriam: menos trabalho por jogador a cada quadro, principalmente no multiplayer.
- As armas de munição do Split faziam o jogo passar por uma checagem extra de munição em todo tiro, de qualquer arma. Não fazem mais.

## 1.0.3 - 2026-11-09 - Correções e desempenho

Correções dos erros relatados na 1.0.2, incluindo o crash ao chamar chefes do jogo, e mais desempenho.

**Desempenho**
- Sistemas que antes rodavam o tempo todo agora só rodam quando são usados: acessórios de lacaios e sentinelas, a armadura do Observador de Estrelas, a Flandre, a Sobrecarga de Mana, os prefixos de armadura e a Armadura Possuída. Criar projéteis ficou mais leve em lutas com muitos tiros.

**Correções**
- Chamar a Plantera, o Golem ou outros chefes do jogo que criam partes (ganchos, mãos, cabeça) fechava o jogo.
- Luva Gélida e Cetro Lacrimoso davam erro no primeiro tiro.
- Starshroom dava erro com uma sentinela em campo.
- Depois de enfrentar o One-Shot, os equipamentos davam um erro repetido sem parar.
- Perto de bancadas de criação de mods aparecia um erro repetido sem parar.
- O Colecionador podia dar erro ao fechar a troca.
- Remendo Vermelho: o golpe extra não saía com armas corpo a corpo.

## 1.0.2 - 2026-11-08 - Correções e desempenho

Uma revisão geral da beta: correção de crashes e erros que apareciam jogando, armas fora do lugar e bastante desempenho, principalmente em celulares mais fracos e no multiplayer.

**Novidades**
- Suporte ao Boss Checklist: com o mod instalado, o Boss Log mostra The Spirit, One-Shot, Menace e Paraffin, e os minichefes Colosso, Breathtaker e Fairyfly, com como invocar, itens de invocação, mensagem de fuga e se já foram vencidos.

**Desempenho**
- Qualidade automática dos efeitos: quando o jogo cai de quadros, a quantidade de partículas, poeira e luzes do Split diminui sozinha e volta aos poucos quando o jogo se recupera.
- Limite de poeira e de luzes do Split por quadro, que acompanha a opção de intensidade dos efeitos visuais.
- Multiplayer bem mais leve: cada jogador a mais no mundo pesa muito menos do que antes.
- Menos peso a cada quadro em efeitos de partículas, relíquias de chefe, projéteis do Spirit, pet Master Spirit, serpentes de ossos da Paraffin, Pedaços do Céu no chão, botões de toque e acessórios e armaduras que só precisam conferir algo de vez em quando.
- Tomo do Monólito: a aura ficou mais leve no multiplayer.

**Correções**
- Abrir o menu de casas com a Menace (o espírito preso na corrente) fechava o jogo. Os NPCs do Split que não são moradores (Menace, Pessoa Ameaçadora, Twilight Walker e os do Spirit e da Paraffin) não aparecem mais no menu de casas.
- Salvar o mundo podia dar erro por causa das bandeiras dos NPCs do Split.
- The Spirit, Menace e Breathtaker agora vão embora quando você morre (antes ficavam no mundo). O Spirit também some se você se afastar demais, como no Split.
- Armas que ficavam separadas da mão, à frente do jogador: Oscilação Ártica, Ruptura Venenosa, Lança de Zircão, Faca Cerimonial, Chikage, Alternador, Foguete Meteorológico, Olho de Belial, Rifle Fotográfico, Razzle-Dazzle, Leque de Flocos de Gelo e Tomo do Monólito.
- Tempestade Estelar: o clarão do tiro não sai mais andando. Cajado Aracnídeo: o projétil segue a curva certa. As raquetes seguem o jogador sem se adiantar.
- Alho: voltou a ser arremessado e, jogado na Corrupção ou no Carmesim, chama o Twilight Walker como no Split.
- Ovelha montada: o corpo voltou a aparecer. A Ovelha de lã arco-íris não dá mais erro.
- Botão de felicidade dos NPCs do Split (Twilight Walker, Menace, Mágico e outros) mostrava um texto quebrado em vez da fala.
- Biomas do Basaltite e do Navio Encalhado davam erro em alguns mundos.
- Erros ao usar ou ao aparecer na tela: Investida do Ballistick, rastros de projéteis da Paraffin e dos lacaios, Hyperboloid (bola de beisebol), Supercrescimento (ataque secundário), Lâmina Flamejante, Tempestade Estelar e Flamaxe (projéteis perseguidores).
- Erros repetidos sem parar: Máscara do Mal e Máscara Vingadora (agora aumentam o dano de lacaio e a velocidade dos chicotes) e Sétimo Elemento durante o Enjoo de Poção.
- A Roda Lunar da Rocha Lunar não reconhecia a classe da arma.
- O Leque de Flocos de Gelo não aplicava a pausa da regeneração de mana.

## 1.0.0 - 2026-11-01 - Beta: até a Paraffin

A primeira versão completa do port: todo o conteúdo do Split 1.0.11 até a Paraffin, revisado e otimizado para o celular.

**Novidades**
- **Mágico**: visitante noturno do hardmode, chega perto do Guia e vai embora de dia. Loja completa do original, com o estoque mudando a cada dia.
- **Leviatã** e **Schwarzwelt**, os espadões pesados de hardmode: o Leviatã dá Postura Ágil ao acertar; o Schwarzwelt solta quatro adagas de sangue por golpe.
- **Ovelha**: bichinho da Neve com 13 cores de lã (três brilham). Pegue com a rede e monte nela; o tênis do One-Shot faz ela correr.
- **Fotografia**: as 12 fotos de criaturas do Split agora contam no álbum, então as páginas podem ser completadas.
- 7 prefixos de armadura de hardmode, a Forja de Explosão Antiga, o Quadro Holográfico e o buff Metal Pesado das armas pesadas.

**Correções**
- Golpes pesados para a esquerda saíam invertidos; agora seguem o lado do jogador e, na volta, a lâmina vira com o fio para fora.
- O personagem escolhido antes de o Split terminar de carregar vinha sem os itens do mod.
- A Paraffin agora morre como no original: explode, deixa um coração de Basaltita no lugar e sai girando; o loot cai onde ela morreu.
- A Menace agora tem a animação de morte do original: explode em faíscas, cai, sai pulando falando a última frase e leva um raio, soltando o guarda-chuva e o corpo queimado.
- Inimigos que morriam sem soltar pedaços agora soltam os do original: Diabrete das Cavernas, Crabcannon, Pirata sem Rosto, Pirata sem Cabeça, Husk, Idler, Moonwalker, Muskeleton, Savage, Shutterbug, Toiler e Unfairy.
- O Toiler voltou a explodir o vaso ao morrer, com estilhaços e fogo; os vasos de Basaltita se partem em cacos e o comum solta moedas em vez de um gêiser.
- A Jaula de Monstros quebrada solta uma bomba que cai e explode antes de libertar o monstro; a jaula da Paraffin se parte com tremor, explosão e pedaços.
- A Prisão de Gelo do One-Shot solta lascas de gelo a cada rachadura e ao quebrar.
- O totem do Cetro do Piromante dá a Bênção do Piromante (+10% de dano, +5 de defesa e regeneração de vida e mana) a quem fica perto, como no original.
- A Ruptura Venenosa ganhou a Fúria Tóxica: cada debuff do alvo deixa os golpes mais rápidos.
- Itens de teste que tinham ficado no mod foram removidos.
- A entrada da segunda forma da Paraffin voltou a ter a explosão e o foco da câmera.
- O foco da câmera nos chefes (Spirit, One-Shot, Menace, Paraffin) e o tremor da tela não apareciam: o jogo reposicionava a tela antes do desenho.
- O Vício Insidioso, a maldição de quando a Paraffin vira Stalker, aparecia sem nome nem descrição (o Quebra-Gelo e o Forjado na Fúria também).
- Com a Parede de Carne viva, a Paraffin se assusta e foge correndo para o lado oposto, como no original.
- O Navio Encalhado podia não aparecer em mundos novos. Agora a área aceita decorações soltas da caverna e, se o mundo abrir sem o navio (inclusive mundos já criados), ele é gerado uma vez ao entrar.
- O Mágico e as adagas do Schwarzwelt travavam no carregamento; a lâmina do Leviatã aparecia com um quadrado preto; o texto do Metal Pesado saía da caixa; o rastro do Eco da Floresta dava erro.

**Desempenho**
- A luta contra a Paraffin, que caía para 10–20 fps, agora fica entre 50 e 60 fps na maior parte do tempo no celular.
- Os tiros dos chefes, as serpentes de ossos e as ondas da Flandre são atualizados todos juntos, e os tiros mais comuns são desenhados pelo próprio jogo.
- Efeitos de armaduras, acessórios, buffs e poções só rodam quando alguém os usa, em vez de conferirem todo inimigo ou projétil a cada quadro.
- Lacaios e projéteis teleguiados usam a busca de alvos do próprio jogo.
- Sons e texturas dos chefes carregam ao entrar no mundo, sem travadas no meio da luta, e a abertura do jogo ficou bem mais curta.

## 0.7.63 - Início do projeto (0.6 a 0.7.63)

Do zero até a versão anterior à beta, o Split foi trazido para o Bunny Loader em lotes, sempre a partir do código e das texturas originais do Split 1.0.11.

- **Chefes**: Spirit, One-Shot, Menace e Paraffin (com as quatro formas), mais os mini-chefes Colosso, Fairyfly e Breathtaker, e inimigos novos em cada bioma.
- **Mundo**: Navio Encalhado na Neve Subterrânea e Domínio do Submundo, com Basaltita, salas, Baú do Campeão e Forja Explosiva.
- **Sistemas**: Fotografia com o Shutterbug e o álbum, Sobrecarga de Mana, golpes pesados com postura, botão de ação secundária e estandartes.
- **NPCs**: Andarilho do Crepúsculo, Genoshi, Astróloga e Shutterbug, com as lojas do original e itens nas lojas dos NPCs do jogo.
- **Itens**: centenas de armas, armaduras, capacetes de combate, acessórios, chás e poções, pets, montarias, asas, ganchos, mobília, quadros, fantasias e caixas de música.
