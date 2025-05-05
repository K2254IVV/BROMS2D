
# BROMS2D - инструмент для сборки s2disasm  
**BROMS2D** — это инструмент для компиляции дизассемблированного Sonic 2 (для **учебных целей**!).  

Основан на:  
- [s2disasm](https://github.com/sonicretro/s2disasm) — дизассемблер исходного кода Sonic 2.  
- [asm68k](https://github.com/GreyLimit/asm68k) — ассемблер для Motorola 68000.  

---

## 📥 Установка  

### Linux / macOS  
```sh
git clone https://github.com/sonicretro/s2disasm.git  
cd s2disasm  
git clone https://github.com/ваш-логин/BROMS2D.git  
mv BROMS2D/buildROM.sh .  
mv BROMS2D/buildROM.lua .  
mkdir -p build_tools  
mv BROMS2D/build_tools/asm68k/ build_tools/  
rm -rf BROMS2D  
echo "Готово! Запустите buildROM.sh"  
```  

### Windows  
1. Скопируйте этот код в `install.bat` и запустите:  
```bat
@echo off
:: BROMS2D Installer for Windows
echo [*] Установка BROMS2D...
if not exist "s2disasm\" (
  git clone https://github.com/sonicretro/s2disasm.git
)
cd s2disasm
if not exist "BROMS2D\" (
  git clone https://github.com/ваш-логин/BROMS2D.git
)
copy /Y BROMS2D\buildROM.bat .
copy /Y BROMS2D\buildROM.lua .
mkdir build_tools 2>nul
xcopy /E /Y BROMS2D\build_tools\asm68k build_tools\asm68k\
rd /s /q BROMS2D
echo [✓] Готово! Запустите buildROM.bat.
pause
```  

---

## 🔨 Особенности BROMS2D  
✅ **Поддержка Sonic 2 (Rev. A/B, Prototypes)**  
✅ **Автоматическая сборка ROM**  
✅ **Гибкая настройка через buildROM.lua**  
✅ **Оптимизированные скрипты для Windows/Linux**  

---

## ⚙️ Как использовать?  
1. Поместите оригинальный ROM в папку `s2disasm` (название: `sonic2.md` или укажите свой в `buildROM.lua`).  
2. Запустите:  
   - **Windows**: `buildROM.bat`  
   - **Linux/macOS**: `./buildROM.sh`  

---

## 📌 Примечания  
- Только для образовательных целей!  
- Требуется **исходный ROM** Sonic 2.  
- Для работы нужен **Lua** (для скриптов компиляции).  

---

Готово! Теперь ваш README отражает суть **BROMS2D** и корректно работает с **s2disasm**. Можно добавить разделы про отладку, лицензию или примеры сборки, если нужно. 🚀
