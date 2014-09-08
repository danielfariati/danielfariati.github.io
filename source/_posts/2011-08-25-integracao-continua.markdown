---
layout: post
title: "Integração Contínua"
date: 2011-08-25 00:00:00 -0300
comments: true
categories: ágil gestão
---
## O que é?

Segundo Martin Fowler, *“Integração Contínua é uma pratica de desenvolvimento de software onde os membros de um time integram seu trabalho frequentemente, geralmente cada pessoa integra pelo menos diariamente – podendo haver múltiplas integrações por dia. Cada integração é verificada por um build automatizado (incluindo testes) para detectar erros de integração o mais rápido possível. Muitos times acham que essa abordagem leva a uma significante redução nos problemas de integração e permite que um time desenvolva software coeso mais rapidamente”.*

Devido ao crescimento de popularidade das metodologias ágeis, a integração contínua tornou-se importante para a comunidade de desenvolvimento de software. Ela facilita a integração, não importando o tamanho da equipe e quantas pessoas estão alterando o código ao mesmo tempo.

<!-- more -->

## Repositórios e versionamento
{% img https://farm6.staticflickr.com/5107/5586120369_5257190402_z.jpg Git to Subversion por Peter Rukavina %}

Um **sistema de controle de versão** (versionamento) tem como finalidade gerenciar diferentes versões do sistema e centralizar seu armazenamento.  Existem muitos sistemas desse tipo disponíveis no mercado, como: CVS, Subversion, Rational ClearCase, Git, Mercurial, Bazaar, entre outros.

Guardar versões facilita muito nossas vidas, pois se cometermos algum erro e só percebermos depois que o código já foi enviado, podemos desfazer as alterações com muita facilidade. O repositório se torna o destino final de tudo que é produzido pela equipe. Chamamos isso de integração.

## Por que usar?

Utilizando as fases convencionais de desenvolvimento (integração apenas depois de completar o desenvolvimento), riscos são submetidos, existem muitos bugs na hora da integração, testes demoram muito mais e, claro, a entrega atrasa.

Com IC, a grande vantagem é o **feedback instantâneo**. A cada commit feito no repositório, o build é gerado automaticamente, os testes são todos executados e as falhas são detectadas. Você pode automatizar o sistema para enviar um e-mail para toda a equipe sempre que houver algum erro no build. Você poderá fazer mudanças sem medo, porque se algo der errado, você saberá rapidamente.

Quando os testes unitários falharem ou aparecer algum bug, os desenvolvedores podem reverter para uma versão sem bugs, sem perder tempo com debugging.  O caos de última hora é evitado, pois os problemas são detectados, e arrumados, continuamente. O feedback é instantâneo sobre a qualidade, funcionalidade e compatibilidade do código que está sendo escrito.

Cauê Guerra, da Caelum, descreveu integração contínua como uma *“integração **automática** com processo de build **automático** e que roda testes de forma **automática** e **automaticamente** detecta falhas em cada pedaço”*.

----

Espero que tenham gostado! Por favor, deixe um comentário com seu feedback.