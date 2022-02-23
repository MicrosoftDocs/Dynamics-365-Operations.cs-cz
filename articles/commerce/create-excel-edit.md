---
title: Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí
description: Toto téma popisuje, jak vytvořit sešit aplikace Excel, abyste mohli upravovat maloobchodní transakce v Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 73a3387d1e7251168002ff683b5b58e0c82a620c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965370"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit sešit aplikace Excel, abyste mohli upravovat maloobchodní transakce v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

K dispozici je předdefinovaná šablona aplikace Excel, ke které mají zákazníci přístup z různých částí systému a používají ji k úpravám a auditu maloobchodních transakcí. Zákazníci si však pro tento účel mohou také vytvořit vlastní sešit aplikace Excel.

## <a name="create-and-configure-an-excel-workbook"></a>Vytvoření a konfigurace sešitu aplikace Excel

Chcete-li vytvořit a konfigurovat sešit aplikace Excel, abyste mohli upravovat maloobchodní transakce, postupujte takto.

1. Otevřete Excel a vytvořte prázdný sešit.
1. Na kartě **Vložit** vyberte **Moje doplňky**.
1. V pravém podokně vyberte odkaz **Přidat informace o serveru**.
1. Zadejte adresu URL serveru a poté vyberte **OK**.
1. Pokud se zobrazí chybová zpráva „Nebyly nalezeny žádné registrace appletů“, problém vyřešíte takto:

    1. V Commerce přejděte na **Správa systému \> Nastavení \> Parametry aplikace Office**.
    1. Na záložce s náhledem **Parametry aplikace** vyberte **Inicializovat parametry aplikace**.
    1. V okně s potvrzovací zprávou vyberte **OK**.
    1. Na záložce s náhledem **Registrované applety** vyberte **Inicializovat registraci appletu**.
    1. Podle potřeby opakujte předchozí tři kroky.

1. Vyberte **Návrh** a potom vyberte **Přidat tabulku**.
1. Na základě dat, která je třeba upravit, vyberte entity, které je nutné přidat do sešitu aplikace Excel pro úpravy. Jako referenci použijte následující tabulku.

    | Typ transakce | Datové entity, které mají být použity |
    |------------------|----------------------|
    | Transakce cash and carry, online objednávky, asynchronní objednávky zákazníka, asynchronní nabídky zákazníka | Transakce (auditovatelné), prodejní transakce (auditovatelné), platební transakce (auditovatelné), daňové transakce (auditovatelné), slevové transakce (auditovatelné), nákladové transakce (auditovatelné) |
    | Odvod do banky | Transakce (auditovatelné), transakce bankovních úhrad (auditovatelné) |
    | Odvod do trezoru | Transakce (auditovatelné), transakce odvodu úhrad do trezoru (auditovatelné) |
    | Výkaz úhrad | Transakce (auditovatelné), transakce výkazu úhrad (auditovatelné) |
    | Příjem, výdaj | Transakce (auditovatelné), příjmové/výdajové transakce (auditovatelné), platební transakce (auditovatelné) |
    | Deklarace počáteční částky, odstranění úhrady, zadání plovoucího zůstatku, změna úhrady, platba faktury, vklad zákazníka | Transakce (auditovatelné), platební transakce (auditovatelné) |

    > [!NOTE]
    > Je důležité, abyste do každého sešitu aplikace Excel přidali pouze jednu datovou entitu. Všechna pole, která jsou označena symbolem klíče, musí být navíc přidána do příslušného sešitu.

1. Po nakonfigurování sešitu použijte požadované filtry. Nezapomeňte použít stejné filtry na všechny listy v souboru. Vyvarujte se načítání velkého množství dat do souboru aplikace Excel. Jinak může být ovlivněn výkon a Excel a váš systém se mohou zpomalit. Jako filtry pro váš soubor doporučujeme vždy použít „Společnost“ a „Číslo výkazu“ nebo „Číslo transakce“.
1. Po nakonfigurování filtrů vyberte **Obnovit** pro načtení dat.
1. Upravte požadovaná data a poté je publikujte. Pokud tlačítko **Publikovat** není k dispozici, některá klíčová pole pravděpodobně nebyla do sešitu aplikace Excel přidána.

## <a name="additional-resources"></a>Další zdroje

[Úpravy a audit transakcí cash and carry a řízení hotovosti](edit-cash-trans.md)

[Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků](edit-order-trans.md)

[Úprava finančních dimenzí pro maloobchodní transakce](edit-financial-dim.md)

[Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí](add-fields-excel.md)
