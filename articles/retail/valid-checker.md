---
title: Kontrola konzistence maloobchodních transakcí
description: Toto téma popisuje funkci kontroly konzistence maloobchodních transakcí v aplikaci Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
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
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "302023"
---
# <a name="retail-transaction-consistency-checker"></a>Kontrola konzistence maloobchodních transakcí


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Toto téma popisuje funkci kontroly konzistence maloobchodních transakcí uvedenou v aplikaci Microsoft Dynamics 365 for Finance and Operations, verze 8.1.3. Kontrola konzistence identifikuje a izoluje nekonzistentní transakce před tím, než se dostanou k procesu zaúčtování výkazů.

Při zaúčtování výkazu v aplikaci Retail může zaúčtování selhat kvůli nekonzistentním datům v tabulkách maloobchodních transakcí. Problém s daty může být způsoben nepředvídanými potížemi v aplikaci Point of Sale (POS), nebo tím, že transakce byly nesprávně naimportovány z POS systémů třetích stran. Příklady toho, jak mohou tyto nekonzistence vypadat, zahrnují: 

  - Celková částka transakce v tabulce záhlaví neodpovídá celkové částce transakce na řádcích.
  - Počet řádků v tabulce záhlaví neodpovídá počtu řádků v tabulce transakcí.
  - Daně v tabulce záhlaví neodpovídají celkové částce daně na řádcích. 
  
Když jsou nekonzistentní transakce přejaty procesem zaúčtování výkazů, vytvoří se nekonzistentní prodejní faktury a deníky plateb, následkem čehož celý proces zaúčtování výkazu selže. Obnovení výkazů z takového stavu představuje složité opravy dat napříč mnoha tabulkami transakcí. Kontrola konzistence maloobchodních transakcí těmto problémům zabraňuje.

Následujíc tabulka znázorňuje proces zaúčtování s kontrolou konzistence transakcí.

![Proces zaúčtování výkazu s kontrolou konzistence transakcí](./media/validchecker.png "Proces zaúčtování výkazu s kontrolou konzistence transakcí")

Dávkové zpracování **Ověřit transakce obchodu** kontroluje konzistenci tabulek maloobchodních transakcí pro následující scénáře:

- Účet odběratele - Ověřuje, že účet odběratele existuje v tabulce maloobchodních transakcí v HQ hlavních datech odběratele.
- Počet řádků - Ověřuje, že počet řádků, jak je zaznamenaný v tabulce záhlaví transakcí, odpovídá počtu řádků v tabulce prodejních transakcí.

## <a name="set-up-the-consistency-checker"></a>Nastavení kontroly konzistence
Nakonfigurujte dávkové zpracování „Ověřit transakce obchodu“ pro periodická spuštění pomocí možností **Maloobchod \> IT pro maloobchod \> Zaúčtování POS**. Dávkovou úlohu lze naplánovat na základě hierarchie organizace obchodu, podobným způsobem, jakým se nastavují zpracování „Vypočítat příkazy v dávkách“ a „Zaúčtovat příkazy v dávkách“. Doporučujeme, abyste nakonfigurovali toto dávkové zpracování tak, aby se spouštělo několikrát denně, a naplánovali jeho spuštění na konec každého provedení úlohy P.

## <a name="results-of-validation-process"></a>Výsledky procesu ověření
Výsledky procesu ověření podle dávkového zpracování jsou označeny na příslušné maloobchodní transakci. Pole **Stav ověření** na záznamu maloobchodní transakce je buď nastaveno na **Úspěšný** nebo **Chyba** a datum posledního spuštění ověření se zobrazí v poli **Poslední čas ověření**.

Chcete-li zobrazit popisnější text chyby související se selháním ověření, zvolte příslušný záznam maloobchodní transakce a klikněte na tlačítko **Chyby ověřování**.

Transakce, u kterých se nezdaří kontrola ověření, a transakce, které ještě nebyly ověřeny, nebudou publikovány do výkazů. Během procesu „Vypočítat výkaz“ budou uživatelé upozorněni, pokud existují transakce, které mohly být zahrnuty ve výkazu, ale nebyly.

Pokud je nalezena chyba ověření, jediným způsobem její opravy je kontaktování podpory Microsoft Support. V dalších verzích bude přidána funkce, aby mohli uživatelé opravit nepodařené záznamy prostřednictvím uživatelského rozhraní. Rovněž budou zpřístupněny funkce protokolování a auditu pro sledování historie úprav.

> [!NOTE]
> V budoucích verzích bude přidáno více pravidel ověření pro podporu více scénářů.
