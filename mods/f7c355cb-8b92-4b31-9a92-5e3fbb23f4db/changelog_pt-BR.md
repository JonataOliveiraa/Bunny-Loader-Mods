# Changelog

## 1.0.2 - 2026-11-08 - Correções e desempenho

Uma revisão geral da beta: erros que apareciam jogando, armas fora do lugar e bastante desempenho, principalmente em celulares mais fracos e no multiplayer.

**Novidades**
- Suporte ao Boss Checklist: com o mod instalado, o Boss Log mostra The Spirit, One-Shot, Menace e Paraffin, e os minichefes Colosso, Breathtaker e Fairyfly, com como invocar, itens de invocação, mensagem de fuga e se já foram vencidos.

**Desempenho**
- Qualidade automática dos efeitos: quando o jogo cai de quadros, a quantidade de partículas, poeira e luzes do Split diminui sozinha e volta aos poucos quando o jogo se recupera.
- Limite de poeira e de luzes criadas pelo Split por quadro, que acompanha a opção de intensidade dos efeitos visuais.
- Cores e vetores fixos usados ao desenhar e criar partículas agora são criados uma vez só, em vez de a cada quadro.
- Multiplayer: os dados do Split de cada jogador ficam guardados; antes eram procurados do zero várias vezes por quadro para cada outro jogador no mundo.
- Tomo do Monólito: a aura confere só o próprio jogador de cada celular, em vez de varrer todos os espaços de jogador.
- Números aleatórios dos efeitos (poeira, faíscas, tiros espalhados) gerados no próprio mod, sem ir ao jogo a cada número.
- Relíquias de chefe desenham com metade das idas ao jogo; os efeitos dos projéteis do Spirit usam a posição da tela guardada no tick.
- Tarefas do jogador que só precisam de conferência de vez em quando (fotografia, solo glacial, inimigos de bioma) deixaram de rodar a cada quadro; o bônus do Crab Rave saiu de um gancho que rodava para todo item.
- Pet Master Spirit: o desenho reaproveita posições, cores e recortes em vez de criar tudo de novo a cada quadro.
- Serpentes de ossos da Paraffin: o corpo segue a cabeça com bem menos idas ao jogo por segmento.
- Pedaços do Céu (Bit of Sky) no chão só brilham perto da tela.
- Botões de toque do Split (ação secundária, Coveiro, Contraptionista, Alternador) conferem primeiro o que é barato, e as armaduras só leem o jogo quando o botão está apertado.

**Correções**
- Armas que ficavam separadas da mão, à frente do jogador: Oscilação Ártica, Ruptura Venenosa, Lança de Zircão, Faca Cerimonial, Chikage, Alternador, Foguete Meteorológico, Olho de Belial, Rifle Fotográfico, Razzle-Dazzle, Leque de Flocos de Gelo e Tomo do Monólito.
- Tempestade Estelar: o clarão do tiro não sai mais andando. Cajado Aracnídeo: o projétil segue a curva certa. As raquetes seguem o jogador sem se adiantar.
- Ovelha montada: o corpo voltou a aparecer. A Ovelha de lã arco-íris não dá mais erro ao ser desenhada.
- Hyperboloid (bola de beisebol), Supercrescimento (ataque secundário), Lâmina Flamejante e Tempestade Estelar/Flamaxe (projéteis perseguidores) davam erro ao serem usados.
- A Máscara do Mal e a Máscara Vingadora davam erro a cada quadro; agora aumentam o dano de lacaio e a velocidade dos chicotes. O Sétimo Elemento tinha o mesmo erro no bônus durante o Enjoo de Poção.
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
