# **Guia Completo para Iniciantes no GitHub e Git**  

Este guia detalhado explica tudo o que você precisa saber para começar a trabalhar com Git e GitHub, desde a instalação até as operações básicas de colaboração.

---

## **1. Instalação do Git**  

### **Para Windows**  
1. Acesse [git-scm.com/downloads](https://git-scm.com/downloads)  
2. Clique em **Download for Windows**  
3. Execute o instalador mantendo todas as opções padrão:  
   - Marque "Use Git from the Windows Command Prompt"  
   - Escolha "Checkout Windows-style, commit Unix-style line endings"  
   - Selecione "Use Windows' default console window"  
4. Após instalação, abra o **Git Bash** e verifique:  
   ```bash
   git --version
   ```
   Isso deve mostrar algo como `git version 2.40.1`

### **Para macOS**  
1. **Opção 1 (recomendada):**  
   Instale via Homebrew (se não tiver, instale primeiro em [brew.sh](https://brew.sh)):  
   ```bash
   brew install git
   ```

2. **Opção 2:**  
   Baixe direto em [git-scm.com/download/mac](https://git-scm.com/download/mac)

3. Verifique no Terminal:  
   ```bash
   git --version
   ```

### **Para Linux (Ubuntu/Debian)**  
1. Atualize e instale:  
   ```bash
   sudo apt update
   sudo apt install git -y
   ```

2. Configure informações adicionais:  
   ```bash
   sudo apt install git-doc git-man git-gui gitk
   ```

3. Verifique:  
   ```bash
   git --version
   ```

---

## **2. Configuração Inicial do Git**  

Execute estes comandos para configurar seu usuário (use o mesmo email do GitHub):  

```bash
git config --global user.name "Seu Nome Completo"
git config --global user.email "seu.email@provedor.com"
```

Configurações úteis adicionais:  
```bash
git config --global core.editor "code --wait"  # Usa VSCode como editor
git config --global init.defaultBranch main   # Define branch padrão como main
```

Para ver todas suas configurações:  
```bash
git config --list
```

---

## **3. Criando e Configurando Conta no GitHub**  

1. Acesse [github.com/signup](https://github.com/signup)  
2. Insira:  
   - Seu email válido  
   - Uma senha segura  
   - Nome de usuário (escolha com cuidado, será sua URL)  
3. Complete a verificação por email  
4. No primeiro login, GitHub oferecerá um tour - recomendo fazer  

---

## **4. Configurando Conexão Segura (SSH)**  

### **Gerando Chaves SSH**  
1. No terminal execute:  
   ```bash
   ssh-keygen -t ed25519 -C "seu.email@provedor.com"
   ```
2. Quando perguntado sobre local para salvar, pressione Enter  
3. Para a senha, você pode deixar em branco (ou criar uma se quiser mais segurança)  

### **Adicionando Chave ao SSH Agent**  
1. Inicie o agent:  
   ```bash
   eval "$(ssh-agent -s)"
   ```
2. Adicione sua chave:  
   ```bash
   ssh-add ~/.ssh/id_ed25519
   ```

### **Adicionando Chave no GitHub**  
1. Exiba e copie sua chave pública:  
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
2. No GitHub:  
   - Acesse Settings > SSH and GPG keys  
   - Clique em "New SSH key"  
   - Cole a chave (começa com `ssh-ed25519`)  
   - Dê um título como "Meu Computador Principal"  

### **Testando a Conexão**  
```bash
ssh -T git@github.com
```
Se aparecer:  
```
Hi seuusuario! You've successfully authenticated...
```
Significa que está tudo certo!

---

## **5. Fazendo Fork de um Repositório**  

O fork cria uma cópia pessoal de qualquer projeto público no GitHub.  

### **Passo a Passo Detalhado:**  
1. Encontre um repositório para contribuir (ex: `https://github.com/octocat/Spoon-Knife`)  
2. No canto superior direito, clique em **Fork**  
3. Se você pertence a organizações, escolha onde o fork será criado (normalmente seu usuário)  
4. Aguarde alguns segundos enquanto o GitHub cria sua cópia  
5. Você será redirecionado para sua versão em `https://github.com/seuusuario/Spoon-Knife`  

### **O Que Acontece Quando Você Faz Fork?**  
- Você recebe uma cópia completa do projeto  
- Pode editar livremente sem afetar o original  
- Pode sincronizar com atualizações do projeto original  
- Pode enviar suas melhorias via Pull Request  

---

## **6. Clonando Seu Repositório Forkado**  
3. No terminal, navegue até a pasta onde quer salvar o projeto e execute:  
   ```bash
   git clone git@github.com:hitalloazevedo/desafio-nodejs.git
   cd desafio-nodejs
   ```
4. Configure o upstream para acompanhar o original:  
   ```bash
   git remote add upstream git@github.com:hitalloazevedo/desafio-nodejs.git
   git remote -v  # Para verificar
   ```

---

## **7. Fluxo de Trabalho Básico**  

### **Comandos Essenciais**  

| Comando | O Que Faz | Quando Usar |
|---------|-----------|-------------|
| `git status` | Mostra alterações | Sempre antes de commitar |
| `git add .` | Prepara todas mudanças | Quando quer incluir arquivos |
| `git commit -m "msg"` | Grava alterações | Após `git add` |
| `git push` | Envia para GitHub | Quando quer compartilhar |
| `git pull` | Atualiza local | Antes de começar a trabalhar |


---

## **Dicas**  

🔹 **Sempre faça pull antes de trabalhar**  
🔹 **Commite com mensagens claras**   

Documentação oficial: [docs.github.com](https://docs.github.com)  

🚀 **Bom desenvolvimento!**
