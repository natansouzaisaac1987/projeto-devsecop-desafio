# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [ ] Secrets Scanning com **Gitleaks**
- [ ] SAST com **Semgrep**
- [ ] SCA com **Grype**
- [ ] Deploy com **GitHub Pages**

## Como a pipeline funciona
> **Substitua este bloco pela sua explicação após implementar a pipeline.**
> Descreva cada step, o que ele faz e por que ele é importante para a segurança.
Pipeline de Segurança (DevSecOps)
Esta esteira de CI/CD foi configurada para garantir a segurança da aplicação antes de qualquer publicação em produção, dividida em três gates (portas) de segurança principais:  
1. Gitleaks (Secrets Scanning / Análise de Segredos)
 O que faz: Examina todo o código-fonte em busca de chaves de API, senhas, tokens ou credenciais que foram salvas diretamente no código por engano.  
 Sua importância está em que se uma credencial for enviada para o GitHub, hackers podem usar robôs para encontrar essa senha e invadir bancos de dados ou serviços da empresa. O Gitleaks impede que o código seja publicado enquanto houver segredos expostos.  
2. Semgrep (SAST - Análise Estática de Segurança de Aplicação)
 O que faz: Analisa a lógica das linhas de código escritas pelos desenvolvedores para encontrar falhas e más práticas (como uso inseguro da função ⁠eval()⁠ ou manipulação direta de ⁠innerHTML⁠).  
 É importante pois permite encontrar e corrigir vulnerabilidades (como ataques de XSS ou injeção de código) ainda no momento do desenvolvimento, garantindo que o sistema seja construído de forma segura desde a base.  
3. Grype (SCA - Análise de Componentes de Software)
 O que faz: Escaneia as bibliotecas e pacotes de terceiros importados no projeto (⁠package.json⁠) para verificar se elas possuem vulnerabilidades conhecidas (CVEs).  
 A importância está em que aplicações modernas usam muitos componentes prontos da comunidade. Se uma biblioteca externa contiver uma falha grave, toda a aplicação ficará exposta; o Grype obriga a manter essas bibliotecas atualizadas nas versões corrigidas.


## URL de Produção
> Adicione aqui o link do GitHub Pages após o deploy.
https://natansouzaisaac1987.github.io/projeto-devsecop-desafio/
