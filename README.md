
# Vue #4: State management med Pinia
👋 Se föreläsningen från i tisdags denna vecka  ✅ 

**Syftet med denna workshop:** 

* Använda Pinia för global state management
* Använda tidigare kunskaper av Vue Router
* Använda Composition API:et istället för Options API:et
* Använd Typescript från start

Dokumentation för Pinia: [https://pinia.vuejs.org/](https://pinia.vuejs.org/)

Bra lathund från Vue Mastery: [https://www.vuemastery.com/vue-cheat-sheet/
](https://www.vuemastery.com/vue-cheat-sheet/
)


# 👩🏽‍💻 Övning 1: State management login/logout 🦸‍♀️

I denna övning ska du använda Pinia till state management för authentisering. Inga tokens, backend. Bara en state i en Pinia-store om användaren är inloggad (true) eller inte (false). Använd dig av följande kod:

store/auth,ts

```
import { defineStore } from 'pinia';

export const useAuthStore = defineStore('auth', {
  state: () => ({
    isLoggedIn: false
  }),
  actions: {
    login() {
      this.isLoggedIn = true;
    },
    logout() {
      this.isLoggedIn = false;
    }
  }
});

```

Använd dina kunskaper från Vue Router och ha tre olika komponenter som visas i ```<router-view>``` beroende om användaren är inloggad eller inte. Dessutom ska du ha en header-komponent som visar Login eller Logout i headera högra del.

```
const routes = [
  { path: '/', component: Home },
  { path: '/login', component: Login },
  { path: '/dashboard', component: Dashboard }
];
```

Dashboard ska alltså vara en protected route som endast ges åtkomst om man är inloggad. Se här om navigation guards => [https://router.vuejs.org/guide/advanced/navigation-guards.htm](https://router.vuejs.org/guide/advanced/navigation-guards.html)l

Godkänd övning ändrar state vid inloggning/utloggning och tar användaren till rätt vy.

# 👩🏽‍💻 Övning 2: Store för produkter 🛒

Förra övningens hade en förhållandevis "liten" store. I denna övning ska du jobba mer med state, getters och action, där din store innehar state management för ett visst antal produkter.

* **state** ska vara en tom lista a produkter. En produkter har ett id, namn och pris
* **getters** ska hämta information om antalet nuvarande produkter samt filtrera produker över ett visst pris
* **actions** ska vara att lägga till en produkt samt ta bort en produkt

Använd nuvarande state, getters and actions för rendera ut i din App/viss komponent. Hur du använder dig av dessa är helt valfritt!

Godkänt övning visar att föreslagna state, getters och actions fungerar i applikationen.


# ✅ Redovisning:
* Du redovisar minst uppgiften för övningen. 
* ***Om du inte kan delta på workshopen, redovisar du ovanstående nästkommande workshop***







