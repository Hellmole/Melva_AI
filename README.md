# MELVA AI – lokální servisní asistent

MELVA AI je lokální inteligentní asistent integrovaný do webové aplikace (Python / Flask).

Důraz kladen na minimální nároky na HW (běžní na standardním CPU a 8 GB RAM) při zachování použitelnosti 

Slouží jako pomocník servisních techniků při diagnostice závad na zařízení na základě historie předchozích oprav.


<img width="801" height="813" alt="obrazek" src="https://github.com/user-attachments/assets/38ba6fcb-1a7c-432a-be9f-465318f9d4a3" />

## Technologie

- Python / Flask – webová aplikace

- Qwen3 1.7B (GGUF) – lokální jazykový model

- llama-cpp-python – provoz AI modelu na CPU

- TXT soubor – zdroj servisních znalostí

- AI pracuje lokálně na serveru bez nutnosti externího API nebo internetového připojení při generování odpovědí.

## Princip fungování

1.Technik zadá dotaz prostřednictvím webového rozhraní /melva/ai.

2.Python prohledá servisní historii v souboru opravy.txt.

3.Vybere tři nejrelevantnější servisní záznamy podle shody slov.

4.Vybrané záznamy a dotaz předá modelu Qwen3.

5.MELVA vygeneruje odpověď v češtině s doporučeným postupem.

Model není dodatečně trénován. Servisní záznamy používá jako kontext při generování odpovědí.
