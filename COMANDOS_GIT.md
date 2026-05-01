# Documentação de Comandos Git

## Fluxo de Trabalho Básico com Git

### 1. Inicializar um Repositório Git
Quando você cria uma pasta nova e quer começar a usar Git:
```bash
git init
```

### 2. Verificar o Status do Repositório
Antes de fazer qualquer coisa, sempre verifique o status para saber quais arquivos foram modificados:
```bash
git status
```
Este comando mostra:
- Arquivos novos (untracked)
- Arquivos modificados
- Arquivos prontos para commit (staged)
- Quantos commits você está à frente da origem

### 3. Adicionar Arquivos (Staging)
Para adicionar arquivos ao "palco" (staging area) antes de fazer commit:
```bash
# Adicionar um arquivo específico
git add nome_do_arquivo.py

# Adicionar todos os arquivos modificados
git add .
```

### 4. Fazer Commit
Após adicionar os arquivos, faça o commit (salvar com mensagem descritiva):
```bash
git commit -m "Descrição clara do que foi feito"
```
Exemplo:
```bash
git commit -m "Adicionar exercícios 1001 até 1010"
```

### 5. Fazer Push (Enviar para Repositório Remoto)
Depois do commit, envie para o GitHub ou outro repositório remoto:
```bash
git push origin master
```
Ou se estiver em outra branch:
```bash
git push origin nome_da_branch
```

---

## Fluxo Completo (Resumido)
Este é o fluxo que você precisa fazer automaticamente:

```bash
# 1. Verificar status
git status

# 2. Adicionar arquivos
git add .

# 3. Fazer commit
git commit -m "Descrição das mudanças"

# 4. Enviar para repositório remoto
git push origin master
```

---

## Comandos Úteis Adicionais

### Ver histórico de commits
```bash
git log
```

### Ver mudanças em um arquivo
```bash
git diff nome_do_arquivo.py
```

### Desfazer alterações
```bash
# Desfazer alterações em um arquivo (antes de adicionar)
git checkout nome_do_arquivo.py

# Remover arquivo da staging area
git reset nome_do_arquivo.py
```

### Configurar informações do usuário (primeira vez)
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"
```

---

## Comandos Usados Neste Projeto

### Terminal 1: Verificação Inicial
```bash
cd e:\Logica
git status
# Resultado: fatal: not a git repository
```

### Terminal 2: Inicialização do Git
```bash
cd e:\Logica\Beecrowd-Python-logica
git init
# Resultado: Reinitialized existing Git repository
```

### Terminal 3: Verificar Status
```bash
git status
# Resultado: On branch master - 1 commit à frente
```

### Terminal 4: Push para o Repositório Remoto
```bash
git push origin master
# Resultado: Sucesso! Enviado para GitHub
```

---

## Dica Final
💡 **Hábito:** Faça um commit sempre que terminar uma funcionalidade ou resolver um problema, mesmo que seja pequeno. Isso facilita rastrear mudanças e reverter se necessário.

**Exemplo de boas mensagens de commit:**
- ✅ "Adicionar validação de entrada no arquivo 1005"
- ✅ "Corrigir erro de cálculo no exercício 1008"
- ❌ "atualizar" (muito vago)
- ❌ "fix" (não descreve o que foi feito)
