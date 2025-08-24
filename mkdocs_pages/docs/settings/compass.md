# Настрока компаса

## Настрока магнитного склонения

**COMPASS_DEC** - Угол, необходимый для компенсации между истинным севером и магнитным севером в радианах


Чтобы перевести угол из градусов и минут в радианы, сначала нужно перевести всё в десятичные градуды, а затем — в радианы.

Данные:

Градусы: +11°

Минуты: 58'

Шаг 1: Переводим минуты в десятичные доли градуса
В одном градусе 60 минут, поэтому:
58' / 60 = 0.9667°

Шаг 2: Складываем чтобы получить десятичные градусы
11° + 0.9667° = 11.9667°

Шаг 3: Переводим десятичные градусы в радианы
Формула для перевода: Радианы = Градусы × (π / 180)
π (Пи) ≈ 3.14159

Итак:
11.9667° × (3.14159 / 180) ≈ 11.9667 × 0.0174533 ≈ 0.2089 радиан

## Конвертер градусов в радианы

<form onsubmit="convertToRadians(); return false;" style="background: #f8f9fa; padding: 20px; border-radius: 8px; margin: 20px 0;">
  <div style="margin-bottom: 15px;">
    <label style="font-weight: bold; display: block; margin-bottom: 5px;">Градусы:</label>
    <input type="number" id="degrees" min="0" max="359" value="0" style="padding: 8px; border: 1px solid #ddd; border-radius: 4px; width: 100px;">
  </div>
  
  <div style="margin-bottom: 15px;">
    <label style="font-weight: bold; display: block; margin-bottom: 5px;">Минуты:</label>
    <input type="number" id="minutes" min="0" max="59" value="0" step="0.1" style="padding: 8px; border: 1px solid #ddd; border-radius: 4px; width: 100px;">
    <span style="color: #666; margin-left: 5px;">(0-59.9)</span>
  </div>
  
  <button type="submit" style="background: #007acc; color: white; padding: 10px 20px; border: none; border-radius: 4px; cursor: pointer; font-weight: bold;">
    Конвертировать в радианы
  </button>
</form>

<div id="conversionResult" style="display: none; background: #e8f5e8; padding: 15px; border-radius: 6px; border-left: 4px solid #4caf50; margin: 20px 0;">
  <h4 style="margin-top: 0; color: #2e7d32;">Результат:</h4>
  <div id="resultDetails"></div>
</div>

<script>
function convertToRadians() {
  // Получаем значения из формы
  const degrees = parseInt(document.getElementById('degrees').value) || 0;
  const minutes = parseFloat(document.getElementById('minutes').value) || 0;
  
  // Проверяем корректность минут
  if (minutes < 0 || minutes >= 60) {
    alert('Минуты должны быть в диапазоне от 0 до 59.9');
    return;
  }
  
  // Конвертируем в десятичные градусы
  const decimalDegrees = degrees + (minutes / 60);
  
  // Конвертируем в радианы
  const radians = decimalDegrees * (Math.PI / 180);
  
  // Показываем результат
  const resultDiv = document.getElementById('conversionResult');
  const detailsDiv = document.getElementById('resultDetails');
  
  detailsDiv.innerHTML = `
    <p><strong>Входные данные:</strong> ${degrees}° ${minutes}'</p>
    <p><strong>Десятичные градусы:</strong> ${decimalDegrees.toFixed(6)}°</p>
    <p><strong>Радианы:</strong> ${radians.toFixed(6)} rad</p>
    <p><strong>Формула:</strong> (${degrees} + ${minutes}/60) × π/180 = ${radians.toFixed(6)}</p>
  `;
  
  resultDiv.style.display = 'block';
}

// Автоматический расчет при изменении значений
document.getElementById('degrees').addEventListener('input', convertToRadians);
document.getElementById('minutes').addEventListener('input', convertToRadians);

// Выполняем первоначальный расчет
convertToRadians();
</script>


