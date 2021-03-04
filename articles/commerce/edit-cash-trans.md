---
title: Úpravy a audit transakcí cash and carry a řízení hotovosti
description: Toto téma popisuje, jak upravit a auditovat transakce cash and carry a řízení hotovosti v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: c809f379dbd6824542d0b1768cfbf44f37461f4c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010192"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Úpravy a audit transakcí cash and carry a řízení hotovosti

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak upravit a auditovat transakce cash and carry a řízení hotovosti v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Zákazníci Dynamics 365 Commerce používají aplikace pokladního místa (POS) prvních stran, stejně jako aplikace prodejního místa (POS) třetích stran. V případě aplikace první strany jsou transakce obchodu načteny do Commerce Headquarters z kanálů pomocí dávkového zpracování. V případě aplikací třetích stran jsou transakce načítány do Commerce Headquarters pomocí integrace. V obou případech musí být po načtení transakcí do Commerce Headquarters proveden proces kontroly konzistence. Tento proces spouští více ověřování transakcí a pouze transakce, které jsou úspěšně ověřeny, jsou načteny do výkazu, aby mohly být zaúčtovány v Commerce Headquarters.

Ověření transakcí obchodu se nemusí zdařit z různých důvodů. Chyba v integračním kódu nebo v aplikaci POS může způsobit nekonzistenci dat. Popřípadě může nekonzistenci dat způsobit chyba uživatele. Uživatel například odstraní produkt poté, co byl synchronizován s kanálem, nebo uživatel uzavře fiskální období, aniž by za dané období zaúčtoval transakce. Zatímco tyto transakce jsou označeny a vyloučeny z výkazů, mohou rušit každodenní zákazníkův proces zaúčtování denního prodeje do financí. V aplikaci Commerce můžete upravit transakce, jejichž ověření se nezdařilo při zachování auditu všech změn.

## <a name="edit-transactions"></a>Upravit transakce

Ve verzi 10.0.5 aplikace Commerce jsou transakce cash and carry, jako prodej a vrácení, jediné transakce, které lze upravit. Objednávky zákazníků a online objednávky nelze upravovat. V aplikaci Commerce verze 10.0.6 a novější lze transakce řízení hotovosti také upravovat.

Chcete-li upravit transakce v Commerce Headquarters, postupujte takto.

1. Nainstalujte [doplněk Microsoft Dynamics Office](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. V Commerce Headquarters otevřete pracovní prostor **Finance obchodu**. Dlaždice **Selhání ověření transakcí** obsahuje předfiltrované zobrazení stránky transakcí, u kterého se nezdařilo jedno nebo více pravidel ověření.
1. Otevřete stránku transakcí a vyberte záznam, jehož ověření se nezdařilo, vyberte **Doplněk Office** a potom vyberte **Upravit vybranou transakci**. Otevře se soubor aplikace Excel, který zobrazuje podrobnosti vybrané transakce. Tento soubor obsahuje následující listy:

    - **Řádky** - Tento list obsahuje záhlaví a řádky produktu transakce a související data transakce.
    - **Platby** - Tento list obsahuje podrobnosti o řádcích platby dané transakce.
    - **Slevy** - Tento list obsahuje podrobnosti transakce související se slevami.
    - **Daně** - Tento list obsahuje podrobnosti transakce související s daněmi.
    - **Náklady** - Tento list obsahuje data transakce související s náklady.

1. V souboru aplikace Excel upravte příslušná pole a poté odešlete data zpět do Commerce Headquarters pomocí funkce publikování doplňku Dynamics Excel. Po publikování dat se změny projeví v systému. Během publikování se neprovádí žádné ověření u změn, které uživatelé provedou.
1. Úplný záznam auditu změn lze zobrazit výběrem možnosti **Zobrazit záznam auditu** v záhlaví **Maloobchodní transakce** pro změny na úrovni záhlaví a v příslušné sekci a provést záznam na příslušné stránce transakce. Například všechny změny související s řádky prodeje se zobrazí na stránce **Prodejní transakce** a všechny změny související s platbami se zobrazí na stránce **Platební transakce**. Pro změny jsou zachovány následující podrobnosti auditu:

    - Datum a čas úpravy
    - Pole
    - Stará hodnota
    - Nová hodnota
    - Změnil/a

1. Po provedení změn a jejich publikování spusťte možnost **Ověřit transakce obchodu** a ověřte, že tyto změny jsou konzistentní a platné.

> [!NOTE]
> Upravovat lze pouze transakce, jejichž ověření se nezdařilo. Chcete-li upravit transakci, která prošla ověřením, změňte stav ověření transakce na **Chyba** nebo **Žádná** a změnu publikujte. Poté můžete upravit data v záhlaví nebo v jakýchkoli jiných podřízených záznamech transakce a publikovat záhlaví nebo záznamy.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Transakce hromadné úpravy, které jsou propojeny s výkazem

Ve verzi 10.0.6 aplikace Commerce a novější je podporována možnost hromadné úpravy transakcí na úrovni výkazů.

Chcete-li hromadně upravit transakce, které jsou propojeny s výkazem v Commerce Headquarters, postupujte takto.

1. Otevřete stránku **Výkazy** a vyberte výkaz obsahující transakce, které je třeba upravit.
1. Vyberte tlačítko **Otevřít Microsoft Office**.
1. V závislosti na tom, co je třeba upravit, vyberte jednu z následujících možností:

    - **Úprava transakcí cash and carry** - Tato možnost umožňuje upravit všechny transakce cash and carry, které jsou zahrnuty ve výkazu. K dispozici jsou následující akci listy aplikace Excel:

        - **Transakce** - Tento list obsahuje všechny informace na úrovni záhlaví pro prodejní transakce.
        - **Prodejní transakce** - Tento list obsahuje všechny informace na úrovni řádku pro prodejní transakce.
        - **Platební transakce** - Tento list obsahuje všechny informace řádku platby pro prodejní transakce.
        - **Slevové transakce** - Tento list obsahuje všechny informace řádku slevy pro prodejní transakce.
        - **Daňové transakce** - Tento list obsahuje všechny informace řádku daně pro prodejní transakce.
        - **Nákladové transakce** - Tento list obsahuje všechny informace řádku nákladů pro prodejní transakce.

    - **Úprava transakcí řízení hotovosti** - Tato možnost umožňuje upravit všechny transakce řízení hotovosti, které jsou zahrnuty ve výkazu. K dispozici jsou následující akci listy aplikace Excel:

        - **Transakce** - Tento list obsahuje všechny informace na úrovni záhlaví pro transakce řízení hotovosti.
        - **Transakce odvodu úhrad do banky** - Tento list obsahuje všechny podrobnosti o transakcích odvodu do banky.
        - **Transakce odvodu úhrad do trezoru** - Tento list obsahuje všechny podrobnosti o transakcích odvodu do trezoru.
        - **Výkaz úhrad** - Tento list obsahuje všechny podrobnosti o transakcích výkazu úhrad.
        - **Transakce příjmů a výdajů** - Tento list obsahuje všechny podrobnosti řádku transakce příjmů a výdajů.
        - **Platební transakce** - Tento list obsahuje všechny informace související s platbou pro operaci **Zaplatit fakturu** a transakci příjmů a výdajů.

1. Upravte požadované transakce.

    > [!NOTE]
    > Ověření nejsou prováděna při publikování hromadně upravených transakcí. Je nutné zajistit, aby byly všechny úpravy přesné a aby byla zachována přesnost dat v jednotlivých listech. Chcete-li například změnit datum transakce pro správu scénářů, kde je uzavřeno fiskální období nebo období zásob pro otevřené transakce, je nutné změnit datum ve všech listech aplikace Excel, které mají sloupec **Obchodní datum**. Chcete-li ověřit transakce po jejich úpravě, můžete zvolit **Znovu ověřit transakce** na stránce **Výkazy**. Než zaúčtujete výkaz, počkejte, až se úloha ověření dokončí.

1. Pokud agregace již byla vygenerována, otevřete stránku **Agregované transakce** a vyberte **Znovu vygenerovat XML prodejní objednávky**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Transakce hromadné úpravy, které nejsou propojeny s výkazem

Verze 10.0.10 aplikace Commerce a novější podporují možnost hromadně upravovat transakce, u kterých selže ověření, ale nejsou propojeny s výkazem.

Chcete-li hromadně upravit transakce, které nejsou propojeny s výkazem v Commerce Headquarters, postupujte takto.

1. Otevřete stránku **Všechny obchody** a vyberte obchod, pro který musí být transakce upraveny.
1. Vyberte tlačítko **Otevřít v Microsoft Office** a poté vyberte **Upravit transakce cash and carry**.
1. Upravte požadované transakce a poté je publikujte.

## <a name="additional-resources"></a>Další zdroje

[Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků](edit-order-trans.md)

[Úprava finančních dimenzí pro maloobchodní transakce](edit-financial-dim.md)

[Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí](create-excel-edit.md)

[Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí](add-fields-excel.md)
