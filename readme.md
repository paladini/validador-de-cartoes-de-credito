# Credit Card Brand Detector / Detector de Bandeiras de Cart├úo

<img alt="Harness Score L0" src="https://paladini.github.io/harness-score/maturity/badge-l0.svg" height="20">
­ƒç║­ƒç© **English**: Detects credit card brand/network based on card number patterns  
­ƒçº­ƒçÀ **Portugu├¬s**: Detecta a bandeira/marca de cart├Áes de cr├®dito baseado no padr├úo do n├║mero

## Supported Brands / Bandeiras Suportadas

Ô£à **11 brands supported / 11 bandeiras suportadas:**

- Visa
- Mastercard  
- American Express
- Diners Club
- Discover
- EnRoute
- JCB
- Voyager
- Hipercard
- Aura
- Elo

## Installation / Instala├º├úo

```bash
npm install credit-card-brand-detector
```

## Usage / Como Usar

### English
```javascript
const { validateCreditCard, detectBrand } = require('credit-card-brand-detector');

// Detect brand and validate
const result = validateCreditCard('4532015112830366');
console.log(result);
// Output: { isValid: true, bandeira: 'Visa' }

// Just detect the brand
const brand = detectBrand('5555555555554444');
console.log(brand); // Output: 'Mastercard'
```

### Portugu├¬s
```javascript
const { validateCreditCard, detectBrand } = require('credit-card-brand-detector');

// Detectar bandeira e validar
const resultado = validateCreditCard('4532015112830366');
console.log(resultado);
// Sa├¡da: { isValid: true, bandeira: 'Visa' }

// Apenas detectar a bandeira
const bandeira = detectBrand('5555555555554444');
console.log(bandeira); // Sa├¡da: 'Mastercard'
```

## API Reference / Refer├¬ncia da API

### `validateCreditCard(cardNumber)`
**English**: Validates a credit card number and detects its brand  
**Portugu├¬s**: Valida um n├║mero de cart├úo de cr├®dito e detecta sua bandeira

**Parameters / Par├ómetros:**
- `cardNumber` (string): Credit card number / N├║mero do cart├úo de cr├®dito

**Returns / Retorna:**
```javascript
{
  isValid: boolean,    // Luhn validation result / Resultado da valida├º├úo Luhn
  bandeira: string|null // Brand name or null / Nome da bandeira ou null
}
```

### `detectBrand(cardNumber)`
**English**: Detects only the credit card brand  
**Portugu├¬s**: Detecta apenas a bandeira do cart├úo de cr├®dito

**Parameters / Par├ómetros:**
- `cardNumber` (string): Credit card number / N├║mero do cart├úo de cr├®dito

**Returns / Retorna:**
- `string|null`: Brand name or null if not recognized / Nome da bandeira ou null se n├úo reconhecida

## Examples / Exemplos

```javascript
// Different card brands / Diferentes bandeiras
console.log(detectBrand('4532015112830366')); // 'Visa'
console.log(detectBrand('5555555555554444')); // 'Mastercard'
console.log(detectBrand('378282246310005'));  // 'American Express'
console.log(detectBrand('30569309025904'));   // 'Diners Club'
console.log(detectBrand('6011111111111117')); // 'Discover'
console.log(detectBrand('201400000000009'));  // 'EnRoute'
console.log(detectBrand('3530111333300000')); // 'JCB'
console.log(detectBrand('8699000000000001')); // 'Voyager'
console.log(detectBrand('6062000000000001')); // 'Hipercard'
console.log(detectBrand('4869330000000001')); // 'Aura'
```

## Features / Caracter├¡sticas

­ƒç║­ƒç© **English:**
- Ô£à Detects 11 major credit card brands
- Ô£à Includes Brazilian brands (Hipercard, Aura, Elo)
- Ô£à Luhn algorithm validation
- Ô£à Handles spaces and hyphens in card numbers
- Ô£à Zero dependencies
- Ô£à Comprehensive unit tests

­ƒçº­ƒçÀ **Portugu├¬s:**
- Ô£à Detecta 11 principais bandeiras de cart├úo
- Ô£à Inclui bandeiras brasileiras (Hipercard, Aura, Elo)
- Ô£à Valida├º├úo por algoritmo de Luhn
- Ô£à Remove espa├ºos e h├¡fens dos n├║meros
- Ô£à Zero depend├¬ncias
- Ô£à Testes unit├írios abrangentes

## License / Licen├ºa

MIT License - see LICENSE file / Licen├ºa MIT - veja o arquivo LICENSE

## About

Developed by Fernando Paladini, using Github Copilot for DIO bootcamp challenge.

## References

- [4devs.com.br](https://www.4devs.com.br/gerador_de_numero_cartao_credito)
- [DIO Courses](https://www.dio.me/)
