<p align="center">
  <img src="./assets/logo.png" alt="Corven" width="364">
</p>

<p align="center">
  <a href="./README.md">English</a> · <strong>Português</strong>
</p>

# Corven

### CSS que envia só o que o teu projecto realmente usa.

O Corven é um compilador de interfaces: gera o mínimo de CSS necessário para construir aplicações rápidas, acessíveis e eficientes, e depois corta tudo o que o teu projecto não toca. Não é uma biblioteca de componentes. Não é um tema. É um compilador, com o CSS como resultado.

---

## O argumento, num único número

O próprio motor JIT do Corven foi apontado a uma página de exemplo real, com instrução para manter só o que essa página usa. Resultado: **173.576 bytes de CSS reduzidos a 16.243 bytes. Uma redução de 90,6%, verificada por um teste automático, não uma estimativa de marketing.** Sem configuração, sem montar um purge à parte, sem ferramenta separada para ligar. Escreves HTML com utility classes; o Corven descobre o que é realmente preciso.

Esse número é a tese inteira do projecto: um framework devia ficar *mais pequeno* à medida que as ferramentas de build ficam mais inteligentes, não maior.

## Porque é que o Corven existe

A maioria dos frameworks CSS resolve "como estilizar rápido". Muito poucos resolvem "como garantir que o CSS que envio daqui a cinco meses continua enxuto, consistente e explicável". O Corven foi construído à volta da segunda pergunta.

- **Utility-first, mas disciplinado.** Cada utility faz exactamente uma coisa (uma classe, uma propriedade CSS). Sem efeitos secundários escondidos, sem classes-mistério que alteram seis propriedades sem se saber.
- **Familiar desde o primeiro dia.** Se conheces o Tailwind, já conheces a maior parte da nomenclatura e da escala do Corven, copiada de propósito, não reinventada só para ser diferente. A curva de aprendizagem é uma restrição de design, não um pormenor esquecido.
- **Um compilador JIT real, construído internamente.** O Corven analisa os teus templates e envia só o CSS que realmente usas, a mesma ideia que o Tailwind popularizou, implementada como compilador próprio do Corven, não como ferramenta de terceiros encaixada à força.
- **Documentação que não pode mentir.** A documentação de referência é gerada directamente a partir do CSS compilado, nunca escrita à mão. Se uma classe existe no build, está documentada. Se não existe, não está.
- **Cascata previsível, sem guerras de especificidade.** Componentes e sobreposições personalizadas usam CSS Cascade Layers nativas em vez de `!important`. A camada que devia ganhar, ganha, sempre, sem adivinhação.
- **Componentes construídos a partir de tokens, nunca CSS arbitrário.** Cada componente é composto pelos mesmos design tokens que as utilities usam. Não há porta das traseiras por onde uma cor hex ou um valor em pixels aparece escondido no sistema.
- **Disciplina de engenharia que podes verificar tu mesmo.** Cada camada vem com testes automáticos de compilação, verificações estruturais e testes de regressão visual, não porque fica bem escrito num README, mas porque bugs reais (um detector de duplicados que não entendia `@media`, uma regra de purge que tratava selectors separados por vírgula como E em vez de OU) foram mesmo apanhados por esta mesma estrutura durante o desenvolvimento. Ver [UPDATES.md](./UPDATES.md).

## O que o torna diferente no mercado

O CSS utility-first resolveu um problema real, mas criou outro: frameworks que crescem sem parar, HTML que fica verboso, e documentação que se desactualiza silenciosamente em relação ao código. A resposta do Corven não é "acrescentar mais funcionalidades". É:

1. **Mentalidade de compilador desde o primeiro dia.** O CSS é o resultado do Corven, não a sua identidade. O scanner e o motor de purge já existem e já medem resultados reais contra uma página real, não um item hipotético do roadmap.
2. **HTML com permissão para ficar mais simples ao longo do tempo.** O plano não é "utilities para sempre". À medida que os padrões se repetem, o Corven está pensado para ajudar a compô-los em componentes reais, sem nunca teres de escrever CSS arbitrário à mão para isso.
3. **Sustentabilidade como consequência mensurável, não como slogan.** Menos CSS, menos regras duplicadas e uma cascata previsível reduzem os bytes transferidos e o trabalho que o browser tem de fazer. O roadmap do Corven inclui reportar isto com uma metodologia real (o modelo Sustainable Web Design), não um score inventado.

## Onde está hoje

As cinco camadas do Core (Tokens, Utilities, Components, Layouts, Pages) estão fechadas: cada uma compila limpa, está coberta por testes automáticos, e tem um exemplo funcional. O compilador JIT está em desenvolvimento activo: o scanner e o motor de purge já existem e já têm resultados reais e medidos (ver acima). **Ainda não existe nenhum pacote instalável.** Isto é cedo. Ver [UPDATES.md](./UPDATES.md) para o registo de desenvolvimento e [ROADMAP.md](./ROADMAP.md) para o que vem a seguir.

Se preferes acompanhar isto a acontecer em vez de confiares numa fotografia do momento, marca o repositório com uma estrela. As actualizações aparecem aqui à medida que marcos reais se fecham, não como marketing.

## Licença

MIT. Ver [LICENSE](./LICENSE).

## Contribuir

Ver [CONTRIBUTING.md](./CONTRIBUTING.md). O projecto ainda não aceita contribuições de código externas, já que ainda não há uma API pública estável para contribuir, mas issues e discussão são bem-vindas.

## Código de Conduta

Ver [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

## Segurança

Ver [SECURITY.md](./SECURITY.md) para como reportar vulnerabilidades.
