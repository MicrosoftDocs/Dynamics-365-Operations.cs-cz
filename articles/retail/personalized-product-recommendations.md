---
title: "Přehled doporučení přizpůsobeného produktu"
description: "Toto téma obsahuje informace o doporučení produktu v aplikaci Dynamics 365 for Retail, která lze zobrazit na zařízení pokladního místa (POS)."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: ce91f675082a34bd5a1e88be7a7af6884dc47add
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="personalized-product-recommendations-overview"></a>Přehled doporučení přizpůsobeného produktu

[!include[banner](includes/banner.md)]


> [!NOTE]
> Aktuální verzi služby doporučení produktu odstraňujeme, protože předěláváme tuto funkci s lepším algoritmem a novějšími funkčnostmi orientovanými na maloobchod. Další informace naleznete v části [Odstraněné nebo zastaralé funkce](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features). 

V aplikaci Dynamics 365 for Retail je možné zobrazit doporučení ohledně produktů v zařízení pokladního místa (POS). Doporučení jsou položky, které mohou zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech. Pro maloobchody s velkým katalogy doporučení pomáhají s objevováním produktu. Vystavením produktů zaměřených na zájmy a nákupní zvyklosti zákazníka mohou doporučení produktu pomáhat maloobchodníkům navýšit prodeje a použít křížové prodeje a zlepšit udržení si zákazníka. V aplikaci Dynamics 365 for Retail jsou doporučení produktu podpořena kognitivní službou a službou Microsoft Azure machine learning.


<a name="scenarios"></a>Scénáře
---------

Doporučení produktu jsou povolena pro následující scénáře POS. Jsou k dispozici v Cloud POS nebo Modern POS (MPOS).

1.  Na stránce **Podrobnosti o produktu**:

-   Pokud obchod asociuje návštěvy se stránkou **Podrobnosti o produktu** při vyhledávání předchozích transakcí napříč různými kanály, modul doporučení navrhuje další položky, které budou pravděpodobně nakoupeny společně.
-   Pokud pracovník obchodu přidá zákazníka k transakci a poté navštíví stránku **Podrobnosti o produktu**, modul doporučení poskytne individuální doporučení prostřednictvím historie transakcí zákazníka.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Na stránce **Transakce**:

-   Modul doporučení navrhuje položky na základě celého seznamu položek v košíku.
-   Pokud pracovník obchodu přidá zákazníka k transakci a, modul doporučení poskytne individuální doporučení prostřednictvím historie transakcí zákazníka a seznamu položek v košíku.

> [!NOTE]
> Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 for Retail. Ovládací prvek **Doporučení** musí být na stránce **Transakce**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Na stránce **Podrobnosti o zákazníkovi**:
    -   Modul doporučení navrhuje položky na základě ID uživatele a položek na seznamu přání uživatele.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Konfigurace aplikace Dynamics 365 for Retail na povolení doporučení POS
Při nastavování doporučení produktu potřebujete provést tyto akce.

1.  Ujistěte se, zda jste vybrali správnou **právnickou osobu**.
2.  Přejděte na **Úložiště entit**, vyberte **Maloobchodní prodej** a poté klikněte na tlačítko **Aktualizovat**. Použijí se ukázková data (nebo vaše data) z vaší provozní databáze a přesunou se do úložiště entit.
3.  Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na **Rozvržení obrazovky**, zvolte rozložení obrazovky, spusťte **Návrhář rozvržení obrazovky**, a potom umístěte ovládací prvek **doporučení**, kam je třeba.

4.  Přejděte na **Parametry maloobchodu**, vyberte **Strojové učení** a vyberte **Ano** v části **Povolit doporučení POS**.
5.  Doporučení na POS zobrazíte spuštěním globální konfigurační úlohy **1110**. Aby se změny návrháře rozvržení obrazovky POS projevily, spusťte úlohu konfigurace kanálu **1070**.

## <a name="how-does-it-work"></a>[]()Jak to funguje?
Když aktualizujete **Úložiště entit**, proběhnou následující akce.

-   Data ve formátu vyžadovaném kognitivními službami je extrahováno z pracovní databáze Dynamics 365 for Retail a odesláno do úložiště entit.
-   Data používá Azure Data Factory (ADF) k vyčištění pomocí skriptů Hive v rámci aktivit ADF. Vyčištěná data jsou uložena do úložiště objektů blob.
-   Data z úložiště objektů blob použije rozhraní API kognitivních služeb k vyzkoušení modelu doporučení.

Při zapnutí možnosti **Povolit doporučení** a spuštění úloh konfigurace jsou uplatněny následující akce.

-   Pověření a ID modelu jsou vybrána z rozhraní API a uložena do provozní databáze Dynamics 365 for Retail v souboru web.config pro AOS a také na maloobchodním serveru.
-   ID a pověření modelu jsou zpřístupněny CRT, aby bylo možné provést volání doporučení produktu z Cloud POS a MPOS.


<a name="see-also"></a>Viz také
--------

[Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS](add-recommendations-control-pos-screen.md)




