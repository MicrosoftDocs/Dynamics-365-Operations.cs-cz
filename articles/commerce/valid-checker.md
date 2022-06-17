---
title: Ověření transakcí obchodu pro výpočet výkazu
description: V tomto článku je popsána funkce pro ověření transakcí obchodu v Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4be40189777a37495f185467050b61af47b684d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890506"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Ověření transakcí obchodu pro výpočet výkazu

[!include [banner](includes/banner.md)]

V tomto článku je popsána funkce pro ověření transakcí obchodu v Microsoft Dynamics 365 Commerce. Proces ověření identifikuje a označí transakce, které způsobí chyby účtování dříve, než jsou vyzvednuty procesem účtování výkazu.

Při pokusu o zaúčtování výkazu může proces ověření selhat z důvodu nekonzistentních dat v tabulkách obchodních transakcí. Zde je několik příkladů faktorů, které mohou způsobit tyto nekonzistence:

- Celková částka transakce v tabulce hlavičky neodpovídá celkové částce transakce na řádcích.
- Počet položek zadaný v tabulce hlavičky neodpovídá počtu položek v tabulce transakcí.
- Daně v tabulce hlavičky neodpovídají celkové částce daně na řádcích. 

Pokud jsou procesem zaúčtování výkazů vyzvednuty nekonzistentní transakce, vytvořené prodejní faktury a deníky plateb mohou způsobit selhání procesu zaúčtování výkazu. Proces **Ověřit transakce obchodu** předchází těmto problémům tím, že zajistí, aby do procesu výpočtu výkazu transakce byly předány pouze transakce, které projdou pravidly ověření transakce.

Následující obrázek ukazuje opakující se denní procesy pro odesílání transakcí, ověřování transakcí a výpočet a účtování výkazů transakcí a procesy na konci dne pro výpočet a účtování finančních výkazů.

![Obrázek ukazující opakující se denní procesy pro odesílání transakcí, ověřování transakcí a výpočet a účtování výkazů transakcí a procesy na konci dne pro výpočet a účtování finančních výkazů](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Uložení pravidel pro ověřování transakcí

Dávkové zpracování **Ověřit transakce obchodu** kontroluje konzistenci tabulek obchodních transakcí na základě následujících pravidel ověření.

> [!NOTE]
> Pravidla ověření budou i nadále přidávána v následujících vydáních.

### <a name="transaction-header-validation-rules"></a>Pravidlo pro ověření hlavičky transakce

V následující tabulce jsou uvedena pravidla ověření hlavičky transakcí, která jsou kontrolována oproti hlavičce maloobchodních transakcí před předáním těchto transakcí do zaúčtování výkazu.

| Pravidlo | Popis |
|-------|-------------|
| Obchodní datum | Toto pravidlo ověřuje, že obchodní datum transakce je spojeno s otevřeným fiskálním obdobím v hlavní knize. |
| Zaokrouhlování měn | Toto pravidlo ověřuje, že částky transakce jsou zaokrouhleny podle pravidla pro zaokrouhlování měn. |
| Účet zákazníka | Toto pravidlo ověřuje, že zákazník použitý v transakci v databázi existuje. |
| Částka slevy | Toto pravidlo ověřuje, že je částka slevy v hlavičce součtem částek slevy na řádcích. |
| Stav zaúčtování fiskálního dokumentu (Brazílie) | Toto pravidlo ověřuje, že fiskální doklad lze úspěšně zaúčtovat. |
| Hrubá částka | Toto pravidlo ověřuje, že je hrubá částka v hlavičce transakce shodná s čistou částkou včetně daně na řádcích transakce plus poplatky. |
| Čistý | Toto pravidlo ověřuje, že je čistá částka v hlavičce transakce shodná s čistou částkou bez daně na řádcích transakce plus poplatky. |
| Čistý + daň | Toto pravidlo ověřuje, že je hrubá částka v hlavičce transakce shodná s čistou částkou bez daně na řádcích transakce plus všechny daně a poplatky. |
| Počet položek | Toto pravidlo ověřuje, že počet položek zadaný v hlavičce transakce odpovídá součtu množství na řádcích transakce. |
| Částka platby | Toto pravidlo ověřuje, že částka platby v hlavičce transakce odpovídá součtu všech platebních transakcí. |
| Výpočet osvobození od daně | Toto pravidlo ověřuje, že součet vypočtené částky a částky osvobozené od daně v řádcích poplatků se rovná původní vypočítané částce. |
| Cena včetně daně | Toto pravidlo ověřuje, že je příznak **Daň je zahrnuta v ceně** konzistentní napříč hlavičkou transakce a daňovými transakcemi. |
| Transakce není prázdná | Toto pravidlo ověřuje, že transakce obsahuje řádky, a že alespoň jeden řádek není prázdný. |
| Nedoplatek/přeplatek | Toto pravidlo ověřuje, že rozdíl mezi hrubou částkou v hlavičce a částkou platby nepřekračuje konfiguraci maximálního nedoplatku/přeplatku. |

### <a name="transaction-line-validation-rules"></a>Pravidla pro ověřování řádku transakce

V následující tabulce jsou uvedena pravidla ověření řádku transakcí, která jsou kontrolována oproti podrobnostem řádku maloobchodních transakcí před předáním těchto transakcí do zaúčtování výkazu.

| Pravidlo | Popis |
|-------|-------------|
| Čárový kód | Toto pravidlo ověřuje, že v databázi existují všechny čárové kódy položek, které jsou použity na řádcích transakce. |
| Řádky poplatku | Toto pravidlo ověřuje, že součet vypočtené částky a částky osvobozené od daně v řádcích poplatků se rovná původní vypočítané částce. |
| Vratky dárkového poukazu | Toto pravidlo ověřuje, že v rámci transakce nedochází k vracení dárkových poukazů. |
| Varianta položky | Toto pravidlo ověřuje, že v databázi existují všechny položky a varianty, které jsou použity na řádcích transakce. |
| Řádková sleva | Toto pravidlo ověřuje, že je částka slevy na řádku součtem slevy transakce. |
| Řádková daň | Toto pravidlo ověřuje, že je částka daně na řádku součtem daní transakce. |
| Záporná cena | Toto pravidlo ověřuje, že na řádcích transakce nejsou použity negativní ceny. |
| Řízení sériovým číslem | Toto pravidlo ověřuje, že se sériové číslo nachází na řádku transakce pro položky řízené sériovým číslem. |
| Dimenze sériového čísla | Toto pravidlo ověřuje, že není zadáno žádné sériové číslo, pokud je dimenze sériového čísla položky neaktivní. |
| Znaménko rozdílu | Toto pravidlo ověřuje, že znaménka množství a čisté částky budou stejné na všech řádcích transakce. |
| Osvobození od daně | Toto pravidlo ověřuje, že se součet ceny položky na řádku a částky osvobozené od daně rovná původní ceně. |
| Přiřazení daňové skupiny | Toto pravidlo ověřuje, že kombinace skupiny DPH a skupiny daně položky vytváří platný daňový průsečík. |
| Měrná jednotka převodu | Toto pravidlo ověřuje, že měrná jednotka všech řádků má platný převod na měrnou jednotku zásob. |

## <a name="enable-the-store-transaction-validation-process"></a>Povolení procesu ověření transakce úložiště

Nakonfigurujte úlohu **Ověřit transakce obchodu** pro periodická spuštění v centrále Commerce (**Retail a Commerce \> Retail a Commerce IT \> Zaúčtování POS**). Dávková úloha je naplánována na základě organizační hierarchie obchodu. Doporučujeme, abyste nakonfigurovali toto dávkové zpracování tak, aby se spouštěl se stejnou frekvencí jako vaše dávkové úlohy **úloha P** a **Výpočet transakčního výkazu**.

## <a name="results-of-the-validation-process"></a>Výsledky procesu ověření

Výsledky dávkového zpracování **Ověřit transakce obchodu** lze zobrazit v každé transakci maloobchodu. Pole **Stav ověření** v záznamu transakce je nastaveno na **Úspěšný**, **Chyba**, nebo **Žádný**. Pole **Čas posledního ověření** zobrazuje datum spuštění posledního ověření.

Následující tabulka popisuje jednotlivé stavy ověření.

| Stav ověření | Popis |
|-------------------|-------------|
| Úspěšný | Všechna povolená ověřovací pravidla jsou splněna. |
| Chyba | Povolené ověřovací pravidlo identifikovalo chybu. Další podrobnosti o chybě zobrazíte výběrem **Chyby ověření** na podokně akcí. |
| Žádný | Typ transakce nevyžaduje použití pravidel ověření. |

![Stránka Transakce obchodu s polem Stav ověření a tlačítkem Chyby ověření.](./media/valid-checker-validation-status-errors.png)

Pouze transakce, které mají stav ověření **Úspěšný**, budou vtaženy do výkazů transakcí. Chcete-li zobrazit transakce, které mají stav **Chyba**, zkontrolujte dlaždici **Selhání ověření Cash and carry** v pracovním prostoru **Finance obchodu**.

![Dlaždice v pracovním prostoru Finance obchodu.](./media/valid-checker-cash-carry-validation-failures.png)

Další informace o tom, jak opravit selhání ověření Cash and carry, viz [Úprava a audit transakcí Cash and carry a správy hotovosti](edit-cash-trans.md).

## <a name="additional-resources"></a>Další prostředky

[Úprava a audit transakcí Cash and carry a správy hotovosti](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
