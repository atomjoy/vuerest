# VueRest - Laravel Vue Vite

Instalacja Laravel 9 z Vue 3 i Vite w katalogu vue-project aplikacji z tłumaczeniami walidacji.

### Pobieranie

```sh
git clone https://github.com/atomjoy/vuerest.git app-vue
```

### Instalacja i kompilacja Vue

Aplikacja Vue znajduje się w katalogu **vue-project** aplikacji i instalowana jest z **npm init vue@latest**. Wersja końcowa kompilowana jest do katalogu **/public/vue** w aplikacji Laravel.

```sh
cd vue-project
npm install
npm run build
cd ..
```

### Wyczyść view cache

Po kompilacji projektu Vue wyczyść view cache w Laravel.

```sh
php artisan view:clear
```

### Uruchom server lokalny aplikacji

W katalogu głównym aplikacji Laravela uruchom server http.

```sh
composer update
php artisan serve
```

## Świeża instalacja Vue

Koniecznie dodaj w katalogu **vue-project** aplikacji Laravel.

```sh
rm -rf vue-project
npm init vue@latest vue-project
php artisan vendor:publish --tag=vueon-config --force
cd vue-project
npm install
npm run build
cd ..
php artisan view:clear
php artisan serve
```

## Wyłączenie view cache w Laravel (dev)

Dodaj do pliku config/view.php

```php
<?php
return [
    'cache' => false,
    // ...
]
```

## Wersje

- v1.0.0 - Czysta instalacja Laravel 9, Vue 3, Vite z tłumaczeniami walidacji.
