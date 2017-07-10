---
title: "Přehled doporučení přizpůsobeného produktu"
description: "V aplikaci Dynamics 365 for Retail je možné zobrazit doporučení ohledně produktů v zařízení pokladního místa (POS). Doporučení jsou položky, které mohou zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech. Pro maloobchody s velkým katalogy doporučení pomáhají s objevováním produktu. Vystavením produktů zaměřených na zájmy a nákupní zvyklosti zákazníka mohou doporučení produktu pomáhat maloobchodníkům navýšit prodeje a použít křížové prodeje a zlepšit udržení si zákazníka. V aplikaci Dynamics 365 for Retail jsou doporučení produktu podpořena kognitivní službou a službou Microsoft Azure machine learning."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 52a16be4b07eafb493c7fd7ad52a6d9d1bb9ee89
ms.openlocfilehash: 492e498572f875da8ee0387b4d9aa52571211bec
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017


---

# <a name="personalized-product-recommendations-overview"></a>Přehled doporučení přizpůsobeného produktu

[!include[banner](includes/banner.md)]


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

**Poznámka** Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 for Retail. Ovládací prvek **Doporučení** musí být na stránce **Transakce**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Na stránce **Podrobnosti o zákazníkovi**:
    -   Modul doporučení navrhuje položky na základě ID uživatele a položek na seznamu přání uživatele.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Konfigurace aplikace Dynamics 365 for Retail na povolení doporučení POS
Při nastavování doporučení produktu potřebujete provést tyto akce.

1.  Ujistěte se, zda jste vybrali správnou **právnickou osobu**.
2.  Přejděte do **úložiště entit**, vyberte **Maloobchodní prodej** a potom klepněte na tlačítko **Aktualizovat**. ** ** Tím se použijí ukázková data (nebo data) z provozní databáze a přesunou do úložiště entita.
3.  Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na **Rozvržení obrazovky, **zvolte rozložení obrazovky, spusťte **Návrhář rozvržení obrazovky**,** ** a potom umístěte ** kontrolu doporučení ** kam je třeba.
4.  Přejděte na **Parametry maloobchodu**, vyberte **Machine-learning**, vyberte **Ano **v části **Povolit doporučení POS**.
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




