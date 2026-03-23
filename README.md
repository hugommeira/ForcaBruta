FORÇA BRUTA v1.0 — Ferramenta Educativa de Segurança de Senhas
Simulador interativo que demonstra, em tempo real e diretamente no navegador, como ataques de força bruta e dicionário funcionam contra senhas protegidas por SHA-256.
O que faz
O usuário digita uma senha curta e a ferramenta tenta quebrá-la testando combinações automaticamente, mostrando visualmente cada tentativa acontecendo. O objetivo é educacional: mostrar na prática por que senhas fracas são perigosas e o que torna uma senha realmente segura.
Funcionalidades principais
Dois modos de ataque

Força Bruta — testa todas as combinações possíveis de caracteres até encontrar a senha
Senhas Comuns — testa uma lista de palavras e senhas frequentemente usadas

Performance máxima no browser

SHA-256 implementado em JavaScript puro e síncrono dentro de Web Workers — sem await, sem overhead de event loop
Paralelismo real: usa todos os núcleos da CPU via navigator.hardwareConcurrency
Cada worker cobre uma faixa independente do espaço de busca, sem sobreposição

Análise educacional em tempo real

Ao digitar uma senha, o analisador mostra instantaneamente a dificuldade, os tipos de caractere detectados, o total de combinações possíveis e o tempo estimado para quebrar
Painel comparativo entre senha fraca (P@ss1) e forte (cavalo-bateria) com números calculados pela velocidade real medida da CPU do usuário
Escala visual com exemplos de senhas reais e seus tempos de quebra

Visualização do ataque

Display de caracteres individuais mostrando qual combinação está sendo testada, com animação de prefixo fixo e dígito ativo
Indicadores por núcleo de CPU mostrando quais workers estão ativos
Barra de progresso com animação

100% offline — nenhum dado é enviado para servidores. Todo o processamento acontece localmente no navegador.
Stack técnica
HTML · CSS · JavaScript vanilla · Web Workers · SubtleCrypto API · Canvas API
