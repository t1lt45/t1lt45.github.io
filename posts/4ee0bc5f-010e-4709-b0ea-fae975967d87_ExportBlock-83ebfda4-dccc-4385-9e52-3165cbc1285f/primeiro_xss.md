# FIRST XSS

### RXSS — My First Official VulnerabilityA Significant Step in My Cybersecurity Journey 🚀**published:** February 3, 2025**reading time:** 5 minutes

Today, I want to share a milestone in my career in CyberSecurity: I identified my first official vulnerability, a Reflected Cross-Site Scripting (RXSS). 🚀

## What is RXSS?

⚪Explaining in a simple and direct way what RXSS is.

— The Reflected Cross-Site Scripting (RXSS) vulnerability happens when a website “reflects” something you type or click on, without verifying that it is safe. This can allow someone malicious to send you a special link. When you click, the site runs hidden code that can, for example, steal your information or do something on the site as if it were you.

⚪Simple example.

— Imagine you are on a search engine. You type in “pizza” and the site responds with “Results for pizza”. If the site doesn’t verify what you’ve typed, someone could create a malicious link that, instead of searching for “pizza”, sends a code to steal your information. And because the site shows it back without checking, the code ends up being executed in your browser.

⚪How to avoid this?

— Websites can fix this by checking everything they receive before showing it back. That way, they ensure that they only display safe things.

The vulnerability exists for sure on vBulletin version 4.2.3, so we’ll use this version in the following references. The entry point for this PHP Object Injection, the vulnerable call to the **unserialize()** PHP function, is located within the **/private.php** script:

## What were your initial analysis and what sparked your curiosity/insight to discover the vulnerability? And when the pop-up came, what was the reaction?

— Starting with my initial analysis: I started with the site even though I’m just “curious” (we need to be curious), as I’m currently looking at some content and studies on Web Attack, I started there, what I already had so far, I started to analyze the behavior of the site, going through all the tabs, buttons, forms, searches, until… On one of these screens I started to put payloads in even without forcing the page too much, until I changed it by the payload used (print below).

`// Used Payload
<script>alert("TILTASx64")</script>`

![image.png](image.png)

*“Entrei em choque quando apareceu o pop-up😁” (I was desperate when the pop-up appeared😁) — I’ll leave you with a small piece of evidence: a screenshot with my "TILTASx64" tag, symbolizing this special moment.*

- Then… BOOM the pop-up on my screen, I froze at first 😅 I couldn’t believe what I was seeing because it was my first discovery, I tested it again to make sure in another browser (still incredulous) and BOOM, pop-up on the screen again.
- Afraid I’d done something wrong, not least because it’s a private project, I went to talk to the person in charge of the project to inform him of the discovery I’d just made.
- And that was basically the process from the moment the project was presented to me and I was included in it.

I will continue to evolve and contribute to meeting the challenges of security in the digital world.

I hope I’ve contributed in some way.

See you!

---

---

---

---

### RXSS — Minha Primeira Vulnerabilidade Oficial

**Um Passo Significativo na Minha Jornada em CyberSecurity 🚀**

**publicado:** 3 de fevereiro de 2025

**tempo de leitura:** 5 minutos

Hoje, quero compartilhar um marco na minha carreira em CyberSecurity: identifiquei minha primeira vulnerabilidade oficial, uma Reflected Cross-Site Scripting (RXSS). 🚀

## O que é RXSS?

⚪ Explicando de forma simples e direta o que é RXSS.

— A vulnerabilidade Reflected Cross-Site Scripting (RXSS) acontece quando um site “reflete” algo que você digitou ou clicou, sem verificar se aquilo é seguro. Isso pode permitir que alguém malicioso envie um link especial para você. Quando você clica, o site executa um código oculto que pode, por exemplo, roubar suas informações ou fazer algo no site como se fosse você.

⚪ Exemplo simples.

— Imagine que você está em um mecanismo de busca. Você digita “pizza” e o site responde com “Resultados para pizza”. Se o site não verificar o que você digitou, alguém pode criar um link malicioso que, em vez de buscar por “pizza”, envie um código para roubar suas informações. E como o site exibe isso de volta sem verificar, o código acaba sendo executado no seu navegador.

⚪ Como evitar isso?

— Os sites podem corrigir isso validando tudo o que recebem antes de exibir de volta. Dessa forma, garantem que apenas conteúdos seguros sejam mostrados.

A vulnerabilidade existe com certeza no vBulletin versão 4.2.3, então usaremos essa versão nas referências a seguir. O ponto de entrada para essa PHP Object Injection, a chamada vulnerável da função **unserialize()** do PHP, está localizada dentro do script **/private.php**:

## Qual foi sua análise inicial e o que despertou sua curiosidade/insight para descobrir a vulnerabilidade? E quando o pop-up apareceu, qual foi a reação?

— Começando pela minha análise inicial: eu comecei pelo site mesmo, até porque sou “curioso” (e precisamos ser curiosos). Como atualmente estou vendo alguns conteúdos e estudos sobre Web Attack, comecei por ali, com o que eu já tinha até então. Passei a analisar o comportamento do site, navegando por todas as abas, botões, formulários, buscas, até que… Em uma dessas telas comecei a inserir payloads, mesmo sem forçar muito a página, até que consegui alterar pelo payload utilizado (print abaixo).

```
// Payload utilizado
<script>alert("TILTASx64")</script>
```

*“Entrei em choque quando apareceu o pop-up 😁” — Vou deixar aqui uma pequena evidência: um print com minha tag "TILTASx64", simbolizando esse momento especial.*

— Então… BOOM, o pop-up na minha tela. Eu travei na hora 😅 Não conseguia acreditar no que estava vendo, porque era minha primeira descoberta. Testei novamente para ter certeza, em outro navegador (ainda incrédulo) e BOOM, pop-up na tela de novo.

— Com medo de ter feito algo errado, até porque é um projeto privado, fui conversar com o responsável pelo projeto para informar a descoberta que eu havia acabado de fazer.

— E basicamente esse foi o processo desde o momento em que o projeto me foi apresentado e eu fui incluído nele.

Vou continuar evoluindo e contribuindo para enfrentar os desafios da segurança no mundo digital.

Espero ter contribuído de alguma forma.

Nos vemos! 🚀