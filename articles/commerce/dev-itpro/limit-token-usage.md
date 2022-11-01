---
title: Omezení používání platebních tokenů
description: Tento článek popisuje funkci, která omezuje použití platebních tokenů v Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709646"
---
# <a name="limit-payment-token-usage"></a>Omezení používání platebních tokenů

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tento článek popisuje funkci, která omezuje použití platebních tokenů v Microsoft Dynamics 365 Commerce. Použití tokenu je omezeno na rozsah prodejní objednávky nebo, pokud je udělen souhlas zákazníka, je uloženo jako karta v evidenci.

## <a name="key-terms"></a>Klíčové podmínky

| Termín | Popis |
|---|---|
| Token | Odkazovaný objekt blob XML v systému Dynamics 365, který ukládá odkazy na platby pro transakční účely. |
| Karta v evidenci | Uložený referenční token karty, který je dohodnutý pro budoucí použití v systému Dynamics 365 nebo platební bráně a který je specifický pro účet zákazníka. |

Omezení použití platebních tokenů se vztahují na jakékoli prostředí, které využívá službu platební brány, kde se používají opakující se tokeny. Základní [Dynamics 365 Payment Connector pro Adyen](adyen-connector.md) používá opakující se platební tokeny k provádění následných akcí objednávky, jako jsou úpravy autorizace a opětovné autorizace.

Abychom pomohli řídit, jak jsou tyto opakující se platební tokeny používány v celém systému, funkce **Omezit použití platebního tokenu na kontext objednávky** omezuje použití opakovaného tokenu na rozsah prodejní objednávky v systému. Když je tato funkce zapnutá, upravuje uživatelské rozhraní (UI) Commerce headquarters tím, že aktualizuje stránky pro zadávání plateb a omezuje možnost vybrat minulé zákaznické platební reference pro použití v nových instancích transakcí.

Tato funkce pomáhá splnit pravidla používání pro některé vydavatele plateb, jako je Visa. Ve svém dokumentu [Základní pravidla Visa a Pravidla produktů a služeb Visa](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) společnost Visa uvádí, že použití platebních tokenů by mělo být omezeno na rozsah transakce, pokud držitel karty nesouhlasí jinak.

Funkce **Omezit použití platebního tokenu na kontext objednávky** je relevantní pouze v případě, že používáte službu platební brány, která využívá opakující se odkazy na platební tokeny.

## <a name="enable-the-feature"></a>Povolení funkce

Chcete-li zapnout funkci **Omezit použití platebního tokenu na kontext objednávky** v Commerce headquarters pro vaše prostředí, přejděte na **Pracovní prostory \> Správa funkcí**, najděte a vyberte **Omezit použití platebního tokenu na kontext objednávky** v seznamu a poté vyberte **Zapnout**.

## <a name="limit-payment-token-usage"></a>Omezení používání platebních tokenů

Když je tato funkce zapnutá, stránky Commerce headquarters, které se používají pro zachycení platebních metod, aktualizují způsob, jakým odkazují na platební metody zákazníka, které má zákazník v evidenci. Tato aktualizace se dotkne především dvou oblastí provozu:

- Jak se zadává evidovaná zákaznická karta jménem zákazníka
- Jak se ukládají informace o platbě vůči zákazníkovi pro budoucí záznamy plateb prodejní objednávky

Když zákazník provádí transakci s kanály Commerce, platební údaje se ukládají s kontextem prodejní objednávky. Kontext prodejní objednávky omezuje platební token tak, že nebude použit jako reference platby proti záznamu zákazníka na platebních stránkách pro nové nebo upravené platby prodejní objednávky v Commerce headquarters.

### <a name="payment-form-changes"></a>Změny platebního formuláře

Když uživatel call centra nebo Commerce headquarters přijme platbu za zákazníka oproti prodejní objednávce, platební stránka obsahuje údaje o výběru způsobu platby. Když je funkce **Omezit použití platebního tokenu na kontext objednávky** zapnutá, pokud uživatel vybere znaménko plus (**+**) na platební stránce se zobrazují pouze uložené záznamy „karta v evidenci“. Změny vyžadují, aby uživatel call centra nebo Commerce headquarters zadal úplné platební údaje, které zákazník uvedl při vyplňování stránky **Zadat platební údaje zákazníka** pro novou transakci prodejní objednávky.

Seznam hodnot pro pole **Číslo** obsahuje pouze odkazy na karty, které jsou spojeny se zákazníkem, který má kartu v evidenci. Filtruje veškeré odkazy na minulé platby, které nespadají do rozsahu prodejní objednávky.

Znaménko plus (**+**) pod polem **Číslo** zůstane dostupné a lze ho použít k zadání platebních informací, které zákazník poskytl pro transakci, která je spojena se zpracovávanou prodejní objednávkou.

### <a name="how-cards-on-file-work"></a>Jak fungují karty v evidenci

Když je funkce **Omezit použití platebního tokenu na kontext objednávky** zapnutá, karta v evidenci je opakující se platební token, který se ukládá do záznamu zákazníka a není omezen na rozsah prodejní objednávky. Karta v evidenci umožňuje uživatelům Commerce headquarters rychlou referenci, když vyplňují platební stránku pro novou platbu prodejní objednávky. Tento odkaz na token je použitelný pouze pro prostředí Dynamics 365. Pro online kanály, které používají službu platební brány, která uživatelům umožňuje uložit platební metodu pro budoucí použití v modulu iFrame platby, platební brána tyto reference bezpečně ukládá jako samostatnou referenci na kartu Dynamics 365 v evidenci.

Například, pokud Dynamics 365 Commerce Payment Connector pro Adyen se používá v online kanálu, zákazníci, kteří při platbě zadávají údaje o své kreditní kartě v modulu iFrame platby, vidí pouze odkazy na karty uložené službou brány pro jejich příštím online nákupu, když jsou ověřeny. Nevidí kartu uloženou v prostředí Dynamics 365 jako možnost v modulu iFrame platby. Podobně, když nakupující zadají objednávku prostřednictvím call centra, jejich online uložené odkazy na karty se uživateli call centra nezobrazují jako možnosti. Uživatel call centra vidí pouze předchozí kartu v referencích ze systému Dynamics 365 (jak odsouhlasil zákazník), aby si je mohl uložit pro budoucí objednávky.

Uživatelé Commerce headquarters mohou uložit kartu v evidenci pro zákazníka tím, že přejdou na **Maloobchod a obchod \> Zákazníci** a vyberou záznam zákaznického účtu. V části **Zákazník \> Nastavení** uživatelé, kteří mají oprávnění ke zpracování platebních stránek, mohou používat stránku zadání **Kreditní karty** pro zadání platební karty, která bude uložena v evidenci pro budoucí transakce. Tato operace pomáhá ušetřit čas při zpracování budoucích plateb prodejní objednávky pro zákazníka. Uživatelé call centra a Commerce headquarters by měli zadávat údaje o kartě na kartě pouze v případě, že zákazník souhlasí s použitím referenční karty pro budoucí transakce.

Zaškrtávací políčko **Uložit pro budoucí použití** v dolní části platebních stránek Commerce headquarters umožňuje uživatelům uložit kartu v evidenci pro budoucí použití. Toto zaškrtávací políčko by mělo být použito pouze v případě, že zákazník souhlasí s používáním karty v evidenci pro budoucí transakce. Můžete zobrazit nebo omezit zaškrtávací políčko **Uložit pro budoucí použití** pomocí možnosti **Povolit evidenci zákaznické karty** na kartě **Platba** stránky **Parametry call centra** v Commerce headquarters. Když je tato možnost nastavena na **Ano**, uživatelé Commerce headquarters, kteří mají oprávnění ke zpracování platebních stránek, mohou uložit kartu v evidenci pomocí zaškrtávacího políčka **Uložit pro budoucí použití**. Když je možnost nastavena na **Ne**, zaškrtávací políčko není dostupné uživatelům Commerce headquarters, kteří mají oprávnění zpracovávat platební stránky. Možnost **Povolit evidenci zákaznické karty** lze použít, pokud chce vaše společnost omezit používání opakujících se tokenů v Commerce headquarters, ale zatím nechce povolit uložení karty v evidenci bez postupu, který zajistí udělení souhlasu zákazníka.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Stránky Commerce headquarters, kde jsou vynucována opakovaná omezení tokenů

Rozsah omezení tokenů ovlivňuje následující oblasti v Commerce headquarters, pokud je tato funkce zapnutá:

- Platební údaje zákazníka na **Prodejní objednávka \> Platby \> Zadat platbu zákazníka**
- Trvalé objednávky
- Platby splátky
- Platby plateb pohledávek platební kartou

### <a name="manage-payment-tokens-archiving-or-removal"></a>Správa platebních tokenů (archivace nebo odstranění)

Platební tokeny, které byly vytvořeny před zapnutím příznaku funkce **Omezit použití platebního tokenu na kontext objednávky** (nebo když byla funkce vypnuta), zůstane v systému „bez rozsahu“ a lze na něj odkazovat ve výběrových seznamech na platební stránce Commerce headquarters. Tyto tokeny lze v Commerce headquarters pravidelně odstraňovat dvěma způsoby:

- Použijte stránku **Archivovat údaje o transakcích kreditní karty** k nastavení úlohy, která pravidelně čistí nebo archivuje platební tokeny. Pokud nastavíte možnost **Odstranit data bez archivace** na **Ano**, tokeny, které splňují nastavení **Minimální stáří transakce (ve dnech)**, budou odstraněny. Další informace viz [Archivace dat transakcí kreditní karty](archive-cc-data.md).
- Použijte novou stránku **Vyčistit tokeny kreditních karet** (**Pohledávky \> Dotazy a zprávy \> Uklidit \> Vyčistit tokeny kreditních karet**), což vám umožní spustit nebo nastavit dávkovou úlohu, která odstraní platební tokeny. Nastavte následující parametry:

    - Hodnota **Minimální stáří tokenu ve dnech** musí být 90 dní nebo více.
    - Nastavení **Spustit na pozadí** lze použít k definování nastavení **Opakování** nebo **Upozornění**.
    - Ke spuštění úlohy pro určitou skupinu lze přiřadit dávkovou skupinu.
    - Pokud je možnost **Soukromé** nastavena na **Ano**, pouze uživatel, který vytváří úlohu, ji může spustit.
    - Nastavení **Ano** u možnosti **Kritická úloha** zajišťuje, že systém aktivně sleduje stav úlohy.

Smazané tokeny nelze načíst. Nastavte pole **Minimální stáří tokenu ve dnech** na rozsah, který vyhovuje nejdelší době trvání transakcí pro vaše prostředí (od autorizace po zachycení nebo vrácení peněz).

## <a name="additional-resources"></a>Další prostředky

[Časté dotazy k platbám](payments-retail.md)

[Modul pokladny](../add-checkout-module.md)

[Platební modul](../payment-module.md)
