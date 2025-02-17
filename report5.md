# Основные команды для управления процессами в Linux

В Linux управление процессами позволяет эффективно мониторить и управлять запущенными приложениями и службами. Вот описание основных команд для работы с процессами.

---

## 1. **`ps`** — просмотр списка процессов

Команда `ps` используется для отображения информации о текущих процессах.

- **Простой вывод всех процессов текущего пользователя:**
  ```bash
  ps
  ```

- **Просмотр всех процессов в системе (включая процессы других пользователей):**
  ```bash
  ps aux
  ```

- **Отображение процессов в дереве:**
  ```bash
  ps aux --forest
  ```

- **Поиск процесса по имени:**
  ```bash
  ps aux | grep <process_name>
  ```

---

## 2. **`top`** — мониторинг процессов в реальном времени

Команда `top` позволяет в реальном времени мониторить ресурсы, потребляемые процессами.

- **Запуск `top` для отображения процессов:**
  ```bash
  top
  ```

  В интерфейсе `top` отображается информация о процессах, загрузке CPU, памяти и других системных метриках.

- **Для выхода из `top`, нажмите `q`.**

- **Сортировка процессов по использованию памяти (按 `M`):**
  Нажмите `M` в интерфейсе `top`, чтобы отсортировать процессы по потреблению памяти.

- **Сортировка процессов по использованию CPU (按 `P`):**
  Нажмите `P` в интерфейсе `top`, чтобы отсортировать процессы по потреблению процессора.

---

## 3. **`kill`** — завершение процесса

Команда `kill` используется для отправки сигнала процессу, обычно для завершения его работы.

- **Завершение процесса по PID (идентификатору процесса):**
  ```bash
  kill <PID>
  ```

- **Принудительное завершение процесса:**
  Если процесс не завершился после отправки обычного сигнала, используйте сигнал `SIGKILL`:
  ```bash
  kill -9 <PID>
  ```

- **Получить PID процесса:**
  Используйте команду `ps` или `top`, чтобы найти PID процесса, который вы хотите завершить.

---

## 4. **`htop`** — улучшенная версия `top`

Команда `htop` предоставляет более удобный и интерактивный интерфейс для мониторинга процессов и их ресурсов.

- **Запуск `htop`:**
  ```bash
  htop
  ```

  В `htop` отображаются процессы в виде списка, с возможностью сортировки и фильтрации по различным критериям (CPU, память, PID и т.д.).

- **Навигация в `htop`:**
  - Используйте стрелки для перемещения по списку процессов.
  - Для завершения процесса, выберите его и нажмите `F9`.
  - Для выхода из `htop`, нажмите `F10`.

  **Важно:** `htop` может потребовать установки на некоторых системах:
  ```bash
  sudo apt install htop    # для Ubuntu/Debian
  sudo yum install htop    # для CentOS/RHEL
  ```

---

Эти команды являются основными инструментами для мониторинга и управления процессами в Linux.
