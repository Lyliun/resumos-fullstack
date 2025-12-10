
---

> O **Passport.js** é um middleware de autenticação para aplicações Node.js, altamente modular e flexível. Ele funciona por meio de **estratégias** (strategies), permitindo autenticação via credenciais locais (usuário/senha), JWT, OAuth (Google, GitHub, Facebook), entre outros.  
> É muito usado com **Express** e pode ser integrado também ao **NestJS** via _passport adapters_.
> 
> Seu principal objetivo é simplificar a autenticação, garantindo segurança e padronização no fluxo de login.

---

# 🧠 **1. Conceito Central**

- É um **middleware leve**, projetado para ser “plugável”.
    
- Baseado em **estratégias** (mais de 500 disponíveis).
    
- Mantém o fluxo de autenticação simples, focando em segurança e flexibilidade.
    
- Não impõe regras sobre sessões, banco de dados ou modelos — você escolhe como armazenar usuários.
    
- Ajuda a proteger rotas e endpoints sensíveis.
    

---

# ⚙️ **2. Fluxo de Funcionamento (Passo a Passo)**

1. **O cliente envia dados de login**  
    (usuário/senha, token JWT, OAuth etc.)
    
2. **O Passport usa uma estratégia**  
    Ex.: LocalStrategy → valida credenciais com o banco.
    
3. **A estratégia retorna sucesso ou falha**
    
    - Sucesso → retorna o objeto do usuário.
        
    - Falha → retorna erro ou “Unauthorized”.
        
4. **Se configurado com sessão:**
    
    - `serializeUser()` salva só um ID na sessão.
        
    - `deserializeUser()` reconstrói o usuário a partir do ID.
        
5. **O usuário autenticado acessa rotas protegidas**  
    via middleware `passport.authenticate()`.
    

---

# 🔑 **3. Principais Estratégias**

### 🔸 Local Strategy

Autenticação por usuário/senha usando bcrypt para validar a hash.

### 🔸 JWT Strategy

Usa tokens assinados com secret ou RSA keys. Ideal para APIs REST e NestJS.

### 🔸 OAuth2 Strategies

Google, GitHub, Facebook, Discord, Twitter etc.  
Bom para login social.

### 🔸 Custom Strategy

Quando você cria seu próprio método de autenticação personalizado.

---

# 🧩 **4. Exemplo Prático — Local Strategy (Fluxo Simplificado)**

`passport.use(new LocalStrategy(   async (username, password, done) => {     const user = await userService.findByUsername(username);     if (!user) return done(null, false);      const match = await bcrypt.compare(password, user.password);     if (!match) return done(null, false);      return done(null, user);   } ));`

Para proteger uma rota:

`app.post('/login', passport.authenticate('local'), (req, res) => {   res.send('Autenticado!'); });`

---

# 🧰 **5. Passport no NestJS (Resumo)**

Nest usa _strategies_ estendendo `PassportStrategy`:

`@Injectable() export class LocalStrategy extends PassportStrategy(Strategy) {   constructor(private authService: AuthService) {     super();   }    async validate(username: string, password: string) {     return await this.authService.validateUser(username, password);   } }`

E protege rotas usando _guards_:

`@UseGuards(AuthGuard('local')) @Post('login') login(@Request() req) {   return req.user; }`

---

# 📌 **6. Lembretes Importantes**

- Passport não faz hash de senha → use **bcrypt**.
    
- Estratégias têm finalidades diferentes — escolha bem.
    
- `passport.authenticate()` deve ser aplicado por rota.
    
- Ao usar JWT, **não use sessões** (stateless).
    
- Em NestJS, sempre use **Guards** para proteger endpoints.
    

---

# 🧠 **7. Boas Práticas**

- Nunca retorne senhas → sempre remova ou sanitize.
    
- Armazene tokens com segurança (HTTP-only cookies ou local storage com cautela).
    
- Em OAuth2, nunca exponha Client Secret no frontend.
    
- Prefira JWT para APIs escaláveis.
    
- Use HTTPS sempre que possível (evita interceptação de tokens).
    

---

# 🧪 **8. Quando Usar Passport?**

Use quando você precisa de:

- Autenticação tradicional (login e senha)
    
- Login social (Google, GitHub etc.)
    
- Estratégias múltiplas combinadas
    
- Fluxo organizado dentro do NestJS
    

Se sua aplicação é muito simples ou usa apenas JWT, você _pode_ fazer sem Passport — mas ele reduz muito o boilerplate.

---

# 📚 **9. Dicas de Estudo**

- Pratique primeiro a estratégia **Local**, depois migre para JWT.
    
- Integre com bcrypt para entender fluxo completo de autenticação.
    
- Se usar Nest, estude Guards (`AuthGuard`) e Decorators (`@Request()`, `@UseGuards`).
    
- Leia logs do Passport → eles ajudam muito a localizar erros de config.
    
- Teste rotas com Insomnia/Postman enviando credenciais erradas para entender o comportamento.

---

# ✨ **10. TL;DR**

- Passport é um middleware modular para autenticação no Node.js.
    
- Ele usa **estratégias** (Local, JWT, OAuth) para validar usuários.
    
- Age como middleware interceptando requisições.
    
- Em NestJS, Passport é integrado via Guards e módulos.
    
- Muito útil para fluxos complexos de login e múltiplos métodos de autenticação.
    

---

# 🏷️ **Tags**

#passport #nodejs #nestjs #auth #authentication #jwt #oauth #segurança #backend #bancoDeDados 