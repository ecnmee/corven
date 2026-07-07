![Corven](./assets/logo.png)

**[English](./README.md) · [Português](./README.pt.md)**

# Corven

### O compilador de CSS que trata cada byte como uma decisão.

O Corven é um compilador de interfaces. Gera o mínimo de CSS necessário para construir aplicações rápidas, acessíveis e eficientes, e nada mais do que isso. Não é uma biblioteca de componentes. Não é um tema. É um compilador, com o CSS como resultado.

---

## Porque é que o Corven existe

A maioria dos frameworks CSS resolve "como estilizar rápido". Muito poucos resolvem "como garantir que o CSS que envio daqui a cinco meses continua enxuto, consistente e explicável". O Corven foi construído à volta da segunda pergunta.

- **Utility-first, mas disciplinado.** Cada utility faz exactamente uma coisa (uma classe, uma propriedade CSS). Sem efeitos secundários escondidos, sem classes-mistério que alteram seis propriedades sem se saber.
- **Familiar desde o primeiro dia.** Se conheces o Tailwind, já conheces a maior parte da nomenclatura e da escala do Corven, copiada de propósito, não reinventada só para ser diferente. A curva de aprendizagem é uma restrição de design, não um pormenor esquecido.
- **Documentação que não pode mentir.** A documentação de referência é gerada directamente a partir do CSS compilado, nunca escrita à mão. Se uma classe existe no build, está documentada. Se não existe, não está. Não há divergência entre o que é publicado e o que está escrito.
- **Cascata previsível, sem guerras de especificidade.** Componentes e sobreposições personalizadas usam CSS Cascade Layers nativas em vez de `!important`. A camada que devia ganhar, ganha, sempre, sem adivinhação.
- **Componentes construídos a partir de tokens, nunca CSS arbitrário.** Cada componente é composto pelos mesmos design tokens que as utilities usam. Não há porta das traseiras por onde uma cor hex ou um valor em pixels aparece escondido no sistema.
- **Disciplina de engenharia que podes verificar tu mesmo.** Cada camada do Core vem com testes automáticos de compilação, verificações estruturais e testes de regressão visual. Não porque fica bem escrito num README, mas porque um bug real (um detector de duplicados que não entendia `@media`) foi mesmo apanhado por esta mesma estrutura durante o desenvolvimento. Ver [UPDATES.md](./UPDATES.md).

## O que o torna diferente no mercado

O CSS utility-first resolveu um problema real, mas criou outro: frameworks que crescem sem parar, HTML que fica verboso, e documentação que se desactualiza silenciosamente em relação ao código. A resposta do Corven não é "acrescentar mais funcionalidades". É:

1. **Mentalidade de compilador desde o primeiro dia.** O CSS é o resultado do Corven, não a sua identidade. É isso que abre caminho para um compilador JIT real, detecção de desperdício em tempo de build, e orçamentos de performance mais tarde, sem ter de os encaixar à força num framework estático que nunca foi pensado para ser compilado.
2. **HTML com permissão para ficar mais simples ao longo do tempo.** O plano não é "utilities para sempre". À medida que os padrões se repetem, o Corven está pensado para ajudar a compô-los em componentes reais, sem nunca teres de escrever CSS arbitrário à mão para isso.
3. **Sustentabilidade como consequência mensurável, não como slogan.** Menos CSS, menos regras duplicadas e uma cascata previsível reduzem os bytes transferidos e o trabalho que o browser tem de fazer. O roadmap do Corven inclui reportar isto com uma metodologia real (o modelo Sustainable Web Design), não um score inventado.

## Onde está hoje

As Camadas 1 a 4 do Core (Tokens, Utilities, Components, Layouts) estão fechadas: cada uma compila limpa, está coberta por testes automáticos, e tem um exemplo funcional. **Ainda não existe nenhum pacote instalável.** Isto é cedo. Ver [UPDATES.md](./UPDATES.md) para o registo de desenvolvimento e [ROADMAP.md](./ROADMAP.md) para o que vem a seguir (compilador JIT, CLI, runtime, DevTools).

Se preferes acompanhar isto a acontecer em vez de confiares numa fotografia do momento, marca o repositório com uma estrela. As actualizações aparecem aqui à medida que marcos reais se fecham, não como marketing.

## Licença

MIT. Ver [LICENSE](./LICENSE).

## Contribuir

Ver [CONTRIBUTING.md](./CONTRIBUTING.md). O projecto ainda não aceita contribuições de código externas, já que ainda não há uma API pública estável para contribuir, mas issues e discussão são bem-vindas.

## Código de Conduta

Ver [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

## Segurança

Ver [SECURITY.md](./SECURITY.md) para como reportar vulnerabilidades.
