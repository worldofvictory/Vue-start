<script setup lang="ts">
import { ref } from 'vue'

type NotificationType = 'email' | 'web' | 'telegram'

const notificationOptions: NotificationType[] = ['email', 'web', 'telegram']

const notificationLabels: Record<NotificationType, string> = {
  email: 'Email',
  web: 'Web',
  telegram: 'Telegram',
}

// Дані, які обрав користувач
const selectedNotifications = ref<NotificationType[]>([])

// Обробка форми
function handleSubmit() {
  console.log('Вибрані варіанти:', selectedNotifications.value)
  // на наступному етапі реалізуємо fetch POST
}
</script>


<template>
  <div class="notification-settings">
    <h2>Scegli il tuo metodo di notificazione</h2>

    <form @submit.prevent="handleSubmit">
      <div class="notification-option" v-for="option in notificationOptions" :key="option">
        <label>
          <input
            type="checkbox"
            :value="option"
            v-model="selectedNotifications"
          />
          {{ notificationLabels[option] }}
        </label>
      </div>

      <button type="submit">Salva</button>
    </form>
  </div>
</template>


<style scoped>
.notification-settings {
  max-width: 100%;
  margin: 2rem auto;
  padding: 60px;
  border: 1px solid #ccc;
  border-radius: 12px;
}
.notification-option {
  display: flex;
  margin-bottom: 1rem;
  align-items: left;
}
</style>

