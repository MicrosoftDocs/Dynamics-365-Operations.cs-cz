---
title: Úprava a audit transakcí maloobchodu
description: V tomto tématu je popsána funkce pro úpravy a audit transakcí maloobchodu.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: f53573b8afb2003f6796930f5877185e533a4715
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693059"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Úprava a audit transakcí maloobchodu

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Zákazníci Dynamics 365 Retail používají aplikace prvních stran, stejně jako pokladní místo (POS) třetích stran. V aplikaci POS první strany jsou transakce maloobchodu načteny do Retail Headquarters z kanálů pomocí dávkového zpracování. U aplikací třetích stran jsou transakce načítány do Retail Headquarters pomocí integrace. V obou případech, po načtení transakcí do Retail Headquarters, je nutné spustit proces kontroly konzistence, který spustí více ověření na transakcích tak, aby do výkazu, který má být zaúčtován v Retail Headquarters, byly načteny pouze úspěšně ověřené transakce. 

Transakce maloobchodu se nedaří ověřit z různých důvodů. Například chyba v integračním kódu nebo chyba v aplikaci POS může způsobit nekonzistentní data. Nebo chyba uživatele, například odstranění produktu po synchronizaci s kanálem nebo uzavření fiskálního období bez zaúčtování maloobchodních transakcí za toto období, může způsobit nekonzistentní data.

Zatímco tyto transakce jsou označeny a vyloučeny z výkazů, mohou transakce rušit každodenní zákazníkův proces zaúčtování denního maloobchodního prodeje do financí.

V aplikaci Retail můžete upravit konkrétní maloobchodní transakce, jejichž ověření se nezdařilo při zachování auditu všech změn. 

## <a name="edit-and-audit-transactions"></a>Úprava a audit transakcí

Ve verzi 10.0.5 aplikace Retail jsou transakce cash and carry, jako prodej a vrácení, jediné transakce, které lze upravit. Úprava objednávek zákazníků nebo online objednávek není podporována. V aplikaci Retail verze 10.0.6 a vyšších jsou také podporovány úpravy transakcí správy hotovosti.

1. Nainstalujte doplněk Dynamics Excel.

2. Přejděte do pracovního prostoru **Finance maloobchodu**. Dlaždice **Selhání ověření transakcí** obsahuje předfiltrované zobrazení formuláře maloobchodních transakcí, u kterého se nezdařilo jedno nebo více pravidel ověření.
 
3. Otevřete formulář. Klikněte na záznam, jehož ověření se nezdařilo, klikněte na **Doplněk Office** a pak klikněte na **Upravit zvolenou transakci**. Otevře se soubor aplikace Excel s podrobnostmi vybrané transakce s následujícími listy:

    - Řádky: Tento list obsahuje záhlaví a řádky produktu a související data transakce.
    - Platby: Tento list obsahuje podrobnosti o řádcích platby dané transakce.
    - Slevy: Tento list obsahuje podrobnosti transakce související se slevami.
    - Daně: Tento list obsahuje podrobnosti transakce související s daněmi.
    - Náklady: Tento list obsahuje data transakce související s náklady.

4. V souboru aplikace Excel upravte příslušná pole a poté odešlete data zpět do Retail Headquarters pomocí funkce publikování doplňku Dynamics Excel. Po publikování se změny projeví v systému. Během publikování se neprovádí žádné ověření u změn, které uživatelé provedou.

5. Úplný záznam auditu změn lze zobrazit kliknutím na **Zobrazit záznam auditu** v záhlaví **Maloobchodní transakce** pro změny na úrovni záhlaví a v příslušné sekci a provést záznam na příslušné stránce transakce. Například všechny změny související s řádky prodeje budou viditelné na stránce **Prodejní transakce**, změny týkající se plateb budou zobrazeny na stránce **Platební transakce** atd. Podrobnosti o auditu, které jsou udržovány pro změny, jsou následující.

   - Datum a čas úpravy
   - Pole 
   - Stará hodnota
   - Nová hodnota
   - Upravil/a

6. Po provedení změn a jejich publikování spusťte znovu možnost **Ověřit transakce obchodu** a ověřte, že provedené změny jsou konzistentní a platné.

> [!NOTE]
> Upravovat lze pouze transakce, jejichž ověření se nezdařilo. Chcete-li upravit transakce, které prošly ověřením, změňte stav ověření transakce, kterou chcete změnit, na **Chyba** nebo **Žádná**, a poté ji budete moci upravit. 


## <a name="bulk-edit-transactions"></a>Hromadná úprava transakcí

Ve verzi 10.0.6 aplikace Retail a vyšší je podporována možnost hromadné úpravy maloobchodních transakcí na úrovni výkazů. 

1. Použijte doplněk aplikace Excel k otevření výkazu s transakcemi, které chcete upravit, pomocí kroků 1-3.

2. Vyberte jednu z níže uvedených možností.

    - **Upravit transakce cash and carry**. Tato možnost umožňuje úpravu všech cash and carry transakcí zahrnutých do výkazu. K dispozici jsou následující akci listy aplikace Excel.
    
       - **Transakce**: Tento list obsahuje všechny informace na úrovni záhlaví pro prodejní transakce.
       - **Prodejní transakce**: Tento list obsahuje všechny informace na úrovni řádků pro prodejní transakce.
       - **Platební transakce**: Tento list obsahuje všechny informace řádků platby pro prodejní transakce.
       - **Slevové transakce**: Tento list obsahuje všechny informace řádků slevy pro prodejní transakce.
       - **Daňové transakce**: Tento list obsahuje všechny informace řádků daně pro prodejní transakce.
       - **Nákladové transakce**: Tento list obsahuje všechny informace řádků nákladů pro prodejní transakce.

    - **Upravit transakce řízení hotovosti**. Tato možnost umožňuje úpravu všech transakcí řízení hotovosti zahrnutých do výkazu. K dispozici jsou následující akci listy aplikace Excel.
     
       - **Transakce**: Tento list obsahuje všechny informace na úrovni záhlaví pro transakce řízení hotovosti.
       - **Transakce odvodu úhrad do banky**: Tento list obsahuje všechny podrobnosti o transakcích odvodu do banky.
       - **Transakce odvodu úhrad do trezoru**: Tento list obsahuje všechny podrobnosti o transakcích odvodu do trezoru.
       - **Výkaz úhrad**: Tento list obsahuje všechny podrobnosti o transakcích výkazu úhrad.
       - **Transakce příjmů/výdajů**: Tento list obsahuje všechny podrobnosti řádku transakce příjmů a výdajů.
       - **Platební transakce**: Tento list obsahuje všechny informace související s platbou pro operaci **Zaplatit fakturu** a transakci příjmů a výdajů.

3.  Ověření nejsou prováděna při publikování hromadně upravených transakcí. Je nutné zajistit, aby byly všechny úpravy přesné a aby byla zachována přesnost dat v jednotlivých listech. Chcete-li například změnit datum transakce pro správu scénářů, kde je uzavřeno fiskální období nebo období zásob pro otevřené maloobchodní transakce, je nutné změnit datum ve všech listech aplikace Excel, které mají sloupec **Obchodní datum**. Chcete-li ověřit transakce po jejich úpravě, můžete použít **Znovu ověřit transakce** na stránce **Výkazy maloobchodu**.
