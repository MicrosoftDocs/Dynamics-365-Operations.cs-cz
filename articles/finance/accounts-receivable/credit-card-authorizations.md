---
title: Nastavení platební karty, autorizace a záznam
description: Tento článek přehled autorizace platební karty v aplikaci Microsoft Dynamics 365 Finance. Obsahuje informace o způsobu nastavení platební služby, přidání platební karty do prodejní objednávky a anulování ověření.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e615d13abf432705e40e5e33deb46ccab26192ae
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012215"
---
# <a name="credit-card-setup-authorization-and-capture"></a>Nastavení platební karty, autorizace a záznam

[!include [banner](../includes/banner.md)]

Tento článek přehled autorizace platební karty v aplikaci Microsoft Dynamics 365 Finance. Obsahuje informace o způsobu nastavení platební služby, přidání platební karty do prodejní objednávky a anulování ověření.

<a name="setting-up-the-credit-card-payment-service"></a>Nastavení služby pro platby platební kartou
------------------------------------------

Pokud chcete použít platební karty, musíte nastavit a aktivovat službu pro platby na stránce Služby pro platby. Služba pro platby funguje jako spojovací článek mezi vaší právnickou osobou a bankou, která zpracovává kreditní kartu odběratele. Musíte spolupracovat s poskytovatelem kreditní karty, který je uveden v poli Konektor platby a nastavit účet u tohoto poskytovatele. Musíte poté nastavit další možnosti na stránce Služby pro platby, nastavit typy platebních karet pro American Express, Discover, MasterCard a Discover na stránce Typy platebních karet a aktivovat zprostředkovatele jako výchozího zprostředkovatele. Je nutné také postupovat podle těchto kroků pro dokončení instalace:
-   Na stránce Parametry pohledávek zadejte parametry pro použití autorizace platební karty.
-   Na stránce Platební podmínky nastavte platební podmínky pro platební karty. V poli Typ platby vyberte Kreditní karta.
-   Na stránce Platební karty odběratele zadejte informace o kreditní kartě odběratele.

## <a name="adding-a-new-credit-card"></a>Přidání nové platební karty
Můžete vytvořit nové záznamy kreditní karty na stránce Odběratelé pomocí polí Odběratel, Nastavení, Platební karta. Můžete také vytvořit záznamy kreditní karty při zadávání prodejních objednávek na stránce Prodejní objednávku pomocí polí Správa, Odběratel, Kreditní karta, Registrační pokladna.

<a name="adding-a-credit-card-to-a-sales-order"></a>Přidání platební karty do prodejní objednávky
-------------------------------------

Platební kartu lze přidat do prodejní objednávky výběrem platební karty ve vyhledávání platební karty na pevné záložce Cena a sleva na stránce Prodejní objednávky. Ke spuštění procesu ověření v podokně akcí na kartě Spravovat vyberte Kreditní karta a Ověřit.

<a name="authorizing-a-credit-card"></a>Autorizace platební karty
-------------------------

Při ověření dochází nejprve k ověření jména držitele karty a potom k potvrzení disponibilního zůstatku. V případě potřeby lze ověřit i hodnotu ověření platební karty a adresu držitele karty. Disponibilní zůstatek odběratele je snížen o částku faktury. Služba pro platby odešle informaci, zda byla kreditní karta přijata nebo odmítnuta. Při fakturaci prodejní objednávky je kreditní karta zatížena (zaznamenána) částkou faktury.

### <a name="card-verification-value"></a>Ověřovací hodnota platební karty

Můžete vyžadovat hodnotu ověření platební karty, která se někdy nazývá bezpečnostní kód karty. Pro American Express se jedná o čtyřcifernou hodnotu. Pro Discover, MasterCard a Visa se jedná o trojmístnou hodnotu.

### <a name="address-verification"></a>Ověření adresy

Informace z ověření adresy jsou vždy odeslány poskytovateli plateb. Můžete se rozhodnout, jaké informace jsou nutné pro transakce, aby byla přijata. Nezapomeňte se zeptat svého poskytovatele, zda tyto informace přijímá. Máte tyto možnosti k ověření adresy:
-   **Vždy přijmout transakci** – přijímat transakce bez ohledu na výsledky ověření adresy.
-   **Držitel účtu** – porovnat jméno držitele karty z informací o společnosti platební karty pro transakci.
-   **Fakturační adresa** – porovnat jméno držitele karty a fakturační adresu z informací o společnosti platební karty pro transakci.
-   **Fakturační PSČ** – porovnat jméno držitele karty, fakturační adresu a PSČ z informací o společnosti platební karty pro transakci.

## <a name="data-support"></a>Podpora dat
Pro každý typ platební karty, který je podporován, můžete určit úroveň podpory dat. Úroveň určuje, nakolik jsou informace o transakci převedeny do služby pro platby. Nezapomeňte se zeptat svého poskytovatele, zda tyto informace poskytuje. Máte tyto možnosti pro úroveň podpory dat:
-   **Úroveň 1** – přenos dat transakce, částky transakce a popisu.
-   **Úroveň 2** – přenos informací 1. úrovně společně s dodací adresou, adresou obchodníka a informací o dani.
-   **Úroveň 3** – přenos všech informací 2. úrovně společně s informací o řádku objednávky.

## <a name="partial-payments"></a>Částečné platby
Pokud dodáváte část objednávky, je zachycena částka z dílčí objednávky, a ověření, které bylo pro částku celé objednávky, je uzavřeno. Nová autorizace je pak odeslána na zbývající částku objednávky, která ještě nebyla expedována.

## <a name="voiding-an-authorization"></a>Anulování autorizace 
Pro anulování autorizace platební karty můžete změnit metodu platby na jinou metodu, která nemá typ Platební karta.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]