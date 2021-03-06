---
title: Kontrola konzistence maloobchodních transakcí
description: Toto téma popisuje funkci kontroly konzistence transakcí v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9a4f03d8cf6696b7e449448704e5360f2ef585b7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803698"
---
# <a name="retail-transaction-consistency-checker"></a>Kontrola konzistence maloobchodních transakcí

[!include [banner](includes/banner.md)]

Toto téma popisuje funkci kontroly konzistence transakcí v aplikaci Microsoft Dynamics 365 Commerce. Kontrola konzistence identifikuje a izoluje nekonzistentní transakce před tím, než se dostanou k procesu zaúčtování výkazů.

Při zaúčtování výkazu může zaúčtování selhat kvůli nekonzistentním datům v tabulkách obchodních transakcí. Problém s daty může být způsoben nepředvídanými potížemi v aplikaci Point of Sale (POS), nebo tím, že transakce byly nesprávně naimportovány z POS systémů třetích stran. Příklady toho, jak mohou tyto nekonzistence vypadat, zahrnují: 

- Celková částka transakce v tabulce záhlaví neodpovídá celkové částce transakce na řádcích.
- Počet řádků v tabulce záhlaví neodpovídá počtu řádků v tabulce transakcí.
- Daně v tabulce záhlaví neodpovídají celkové částce daně na řádcích. 

Když jsou nekonzistentní transakce přejaty procesem zaúčtování výkazů, vytvoří se nekonzistentní prodejní faktury a deníky plateb, následkem čehož celý proces zaúčtování výkazu selže. Obnovení výkazů z takového stavu představuje složité opravy dat napříč mnoha tabulkami transakcí. Kontrola konzistence transakcí těmto problémům zabraňuje.

Následujíc tabulka znázorňuje proces zaúčtování s kontrolou konzistence transakcí.

![Proces zaúčtování výpisu pomocí kontroly konzistence transakce](./media/validchecker.png "Proces zaúčtování výpisu pomocí kontroly konzistence maloobchodní transakce")

Dávkové zpracování **Ověřit transakce obchodu** kontroluje konzistenci tabulek obchodních transakcí pro následující scénáře:

- **Účet odběratele** - Ověřuje, že účet odběratele existuje v tabulce transakcí v HQ hlavních datech odběratele.
- **Počet řádků** - Ověřuje, že počet řádků, jak je zaznamenaný v tabulce záhlaví transakcí, odpovídá počtu řádků v tabulce prodejních transakcí.
- **Cena zahrnuje daň** - Potvrzuje, že parametr **Cena zahrnuje daň** je konzistentní napříč řádky transakcí a cena na řádku prodeje je v souladu s konfigurací ceny zahrnující daň a osvobození od daně.
- **Částka platby** - Ověří, že záznamy o platbách odpovídají částce platby v záhlaví, a zároveň zohlední konfiguraci pro zaokrouhlování haléřů v hlavní knize.
- **Hrubá částka** - Ověří, že hrubá částka v záhlaví je součtem čistých částek na řádcích plus částka daně, a zároveň zohlední konfiguraci pro zaokrouhlování haléřů v hlavní knize.
- **Čistá částka** - Ověří, že čistá částka v záhlaví je součtem čistých částek na řádcích, a zároveň zohlední konfiguraci pro zaokrouhlování haléřů v hlavní knize.
- **Nedoplatek/přeplatek** – Ověřuje, že rozdíl mezi hrubou částkou v záhlaví a částkou platby nepřekračuje konfiguraci maximálního nedoplatku/přeplatku, a zároveň zohlední konfiguraci pro zaokrouhlování haléřů v hlavní knize.
- **Částka slevy** – Ověřuje, že částka slevy v tabulkách slev a částka slevy v tabulkách řádků transakcí jsou konzistentní a že částka slevy v záhlaví je součtem částek slev na řádcích, a zároveň zohlední konfiguraci pro zaokrouhlování haléřů v hlavní knize.
- **Řádková sleva** - Ověřuje, že řádková sleva na řádku transakce je součtem všech řádků v tabulce slev, která odpovídá řádku transakce.
- **Položka dárkového poukazu** – Commerce nepodporuje vrácení položek dárkového poukazu. Nicméně zůstatek na dárkovém poukazu lze vyplatit v hotovosti. U jakékoliv položky dárkového poukazu, která je zpracována jako řádek vrácení namísto řádku vyplacení v hotovosti, se proces zaúčtování výkazů nezdaří. Proces ověřování pro položky dárkového poukazu pomáhá zaručit, že jediné položky řádku vrácení dárkového poukazu v tabulce transakcí jsou řádky vyplacení dárkového poukazu.
- **Záporná cena** – Ověřuje, že neexistují žádné řádky transakce s negativní cenou.
- **Položka a varianta** – Ověřuje, že položky a varianty na řádcích transakce existují v hlavním souboru položek a variant.
- **Částka daně** - Ověřuje, že se záznamy daně shodují s částkami daně na řádcích.
- **Sériové číslo** - Ověřuje, že se sériové číslo nachází v řádcích transakce pro položky řízené sériovým číslem.
- **Podepsat** - Ověřuje, že znaménko množství a čistá částka budou stejné ve všech řádcích transakce.
- **Obchodní datum** – Ověřuje, zda jsou finanční období pro všechna obchodní data pro transakce otevřená.
- **Poplatky** - Ověřuje, že částka poplatku záhlaví a řádku odpovídá ceně, včetně konfigurace daně a osvobození od daně.

## <a name="set-up-the-consistency-checker"></a>Nastavení kontroly konzistence

Nakonfigurujte dávkové zpracování „Ověřit transakce obchodu“ pro periodická spuštění pomocí možností **Retail a Commerce \> IT pro Retail a Commerce \> Zaúčtování POS**. Dávkovou úlohu lze naplánovat na základě hierarchie organizace obchodu, podobným způsobem, jakým se nastavují zpracování „Vypočítat příkazy v dávkách“ a „Zaúčtovat příkazy v dávkách“. Doporučujeme, abyste nakonfigurovali toto dávkové zpracování tak, aby se spouštělo několikrát denně, a naplánovali jeho spuštění na konec každého provedení úlohy P.

## <a name="results-of-validation-process"></a>Výsledky procesu ověření

Výsledky procesu ověření podle dávkového zpracování jsou označeny na příslušné transakci. Pole **Stav ověření** na záznamu transakce je buď nastaveno na **Úspěšný** nebo **Chyba** a datum posledního spuštění ověření se zobrazí v poli **Poslední čas ověření**.

Chcete-li zobrazit popisnější text chyby související se selháním ověření, zvolte příslušný záznam transakce a klikněte na tlačítko **Chyby ověřování**.

Transakce, u kterých se nezdaří kontrola ověření, a transakce, které ještě nebyly ověřeny, nebudou publikovány do výkazů. Během procesu „Vypočítat výkaz“ budou uživatelé upozorněni, pokud existují transakce, které mohly být zahrnuty ve výkazu, ale nebyly.

Pokud je nalezena chyba ověření, jediným způsobem její opravy je kontaktování podpory Microsoft Support. V dalších verzích bude přidána funkce, aby mohli uživatelé opravit nepodařené záznamy prostřednictvím uživatelského rozhraní. Rovněž budou zpřístupněny funkce protokolování a auditu pro sledování historie úprav.

> [!NOTE]
> V budoucích verzích bude přidáno více pravidel ověření pro podporu více scénářů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]