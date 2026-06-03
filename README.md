# Calculadora CI

![PHP CI](https://github.com/H1kik0m0r1/Parcial2/actions/workflows/php-ci.yml/badge.svg)

**Integrantes:**
- Lina Marcela Torres Sánchez

**Repositorio público:** https://github.com/H1kik0m0r1/Parcial2

---

## Estructura del Proyecto

```
PARCIAL/
├── .github/
│   └── workflows/
│       └── php-ci.yml              # Pipeline de Integración Continua
├── src/
│   └── Calculadora.php             # Clase Calculadora con operaciones básicas
├── tests/
│   └── CalculadoraTest.php         # Pruebas unitarias con PHPUnit
├── composer.json                   # Dependencias del proyecto
├── README.md                       # Este archivo
```

## Pruebas Unitarias

| # | Prueba | Descripción | Resultado |
|---|--------|-------------|-----------|
| 1 | `testSuma` | Verifica que `sumar(2, 3)` retorne `5` | ✓ Pasó |
| 2 | `testResta` | Verifica que `restar(4, 3)` retorne `1` | ✓ Pasó |
| 3 | `testMultiplicacion` | Verifica que `multiplicar(4, 3)` retorne `12` | ✓ Pasó |
| 4 | `testDivision` | Verifica que `dividir(6, 3)` retorne `2` | ✓ Pasó |
| 5 | `testDivisionPorCeroLanzaExcepcion` | Verifica que `dividir(5, 0)` lance `InvalidArgumentException` | ✓ Pasó |

## Pipeline de Integración Continua

El workflow de GitHub Actions (`php-ci.yml`) ejecuta los siguientes pasos:

1. **Descargar Código** - Checkout del repositorio
2. **Configurar PHP** - Entorno PHP 8.2 con extensiones mbstring y xml
3. **Instalar Dependencias** - `composer install`
4. **Ejecutar Pruebas** - `./vendor/bin/phpunit tests`

El pipeline se activa en cada push o pull request a las ramas `main` y `desarrollo`.
