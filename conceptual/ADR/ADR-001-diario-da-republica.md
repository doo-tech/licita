# ADR-001 — Relação com o Diário da República

**Status:** Aceite  
**Data:** 2026-05-22  
**Decisores:** Equipa Licita  

---

## Contexto

Em Angola, a publicação de concursos públicos no Diário da República é uma obrigação legal para que o concurso tenha validade jurídica. Qualquer processo de contratação pública que não passe por esse canal pode ser contestado por participantes ou entidades fiscalizadoras, independentemente da qualidade do processo em si.

O Licita é uma plataforma de gestão de concursos públicos end-to-end. A questão colocada foi: qual o papel do Diário da República no modelo operacional da plataforma?

---

## Decisão

O Licita **coexiste** com o Diário da República. Não o substitui nem o ignora.

Concretamente:

1. Quando uma instituição pública finaliza a criação de um concurso dentro do Licita, o sistema gera automaticamente o documento oficial no formato exigido pelo Diário da República.
2. A submissão desse documento ao Diário é feita pelo responsável da instituição como passo obrigatório e explícito dentro do fluxo do processo.
3. O concurso **não avança** para a fase de recepção de propostas até que a confirmação de publicação no Diário seja registada na plataforma.
4. O Licita opera como o sistema de gestão operacional real; o Diário mantém a sua função de arquivo jurídico oficial.

---

## Alternativas Consideradas

### Alternativa A — Licita como canal oficial (substituição do Diário)

Tornar a publicação dentro do Licita juridicamente equivalente à publicação no Diário da República, eliminando a dependência deste. Exigiria reconhecimento formal por parte do Estado angolano e actualização do quadro legislativo aplicável à contratação pública.

**Rejeitada.** A dependência de mudança legislativa coloca o lançamento do produto fora do controlo da equipa. O tempo e a incerteza associados a esse processo inviabilizam qualquer planeamento de produto a curto e médio prazo.

### Alternativa B — Ignorar o Diário da República

Operar o Licita sem qualquer integração com o Diário, assumindo que a plataforma gera legitimidade suficiente por si própria.

**Rejeitada.** Viola a lei vigente. Expõe os concursos publicados exclusivamente no Licita a contestação jurídica, o que destrói a proposta de valor da plataforma.

---

## Consequências

**Positivas:**

- O produto pode ser lançado sem depender de alterações legislativas.
- A fricção de cumprir a obrigação legal é absorvida pelo sistema — o utilizador não precisa de saber como gerar o documento correcto.
- O Licita posiciona-se como complementar ao Estado, não como desafiante, o que facilita adopção institucional.

**Negativas / Limitações:**

- Existe sempre um passo manual de confirmação de publicação no Diário. Não é possível automatizar completamente esta etapa enquanto o Diário não disponibilizar uma API pública de submissão.
- O avanço do concurso fica dependente de uma acção humana externa à plataforma, introduzindo um ponto de atraso potencial.
- Se no futuro o Estado criar um portal de contratação pública oficial, esta decisão terá de ser reavaliada.

---

## Revisão

Esta decisão deve ser reavaliada se:

- O Diário da República disponibilizar uma API de submissão programática.
- O Estado angolano publicar legislação que reconheça plataformas electrónicas como canal oficial equivalente ao Diário.
- O Licita for adoptado como plataforma oficial por decreto.
