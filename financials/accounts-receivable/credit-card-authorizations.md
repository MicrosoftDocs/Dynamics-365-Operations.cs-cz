---
title: "Nastavení platební karty, autorizace a záznam"
description: "Tento článek přehled autorizace platební karty v aplikaci Microsoft Dynamics AX. Obsahuje informace o způsobu nastavení platební služby, přidání platební karty do prodejní objednávky a anulování ověření."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 40d950b04511e85d05106c274d1580a3daac7af7
ms.lasthandoff: 03/31/2017


---

# <a name="credit-card-setup-authorization-and-capture"></a>Nastavení platební karty, autorizace a záznam

[!include[banner](../includes/banner.md)]


Tento článek přehled autorizace platební karty v aplikaci Microsoft Dynamics AX. Obsahuje informace o způsobu nastavení platební služby, přidání platební karty do prodejní objednávky a anulování ověření.

<a name="setting-up-the-credit-card-payment-service"></a>Nastavení služby pro platby platební kartou
------------------------------------------

Pokud chcete použít platební karty, musíte nastavit a aktivovat službu pro platby na stránce Služby pro platby. Služba pro platby funguje jako spojovací článek mezi vaší právnickou osobou a bankou, která zpracovává kreditní kartu odběratele. Musíte spolupracovat s poskytovatelem kreditní karty, který je uveden v poli Konektor platby a nastavit účet u tohoto poskytovatele. Musíte poté nastavit další možnosti na stránce Služby pro platby, nastavit typy platebních karet pro American Express, Discover, MasterCard a Discover na stránce Typy platebních karet a aktivovat zprostředkovatele jako výchozího zprostředkovatele. Je nutné také postupovat podle těchto kroků pro dokončení instalace:
-   Na stránce Parametry pohledávek zadejte parametry pro použití autorizace platební karty.
-   Na stránce Platební podmínky nastavte platební podmínky pro platební karty. V poli Typ platby vyberte Kreditní karta.
-   Na stránce Platební karty odběratele zadejte informace o kreditní kartě odběratele.

## <a name="adding-a-new-credit-card"></a>Přidání nové platební karty
Můžete vytvořit nové záznamy kreditní karty na stránce Odběratelé pomocí polí Odběratel, Nastavení, Platební karta. Můžete také vytvořit záznamy kreditní karty při zadávání prodejních objednávek na stránce Prodejní objednávku pomocí polí Správa, Odběratel, Kreditní karta, Registrační pokladna.
Přidání platební karty do prodejní objednávky
-------------------------------------

Platební kartu lze přidat do prodejní objednávky výběrem platební karty ve vyhledávání platební karty na pevné záložce Cena a sleva na stránce Prodejní objednávky. Ke spuštění procesu ověření v podokně akcí na kartě Spravovat vyberte Kreditní karta a Ověřit.
Autorizace platební karty
-------------------------

Při ověření dochází nejprve k ověření jména držitele karty a potom k potvrzení disponibilního zůstatku. V případě potřeby lze ověřit i hodnotu ověření platební karty a adresu držitele karty. Disponibilní zůstatek odběratele je snížen o částku faktury. Služba pro platby odešle informaci, zda byla kreditní karta přijata nebo odmítnuta. Při fakturaci prodejní objednávky je kreditní karta zatížena (zaznamenána) částkou faktury.

### <a name="card-verification-value"></a>Ověřovací hodnota platební karty

Můžete vyžadovat hodnotu ověření platební karty, která se někdy nazývá bezpečnostní kód karty. Pro American Express se jedná o čtyřcifernou hodnotu. Pro Discover, MasterCard a Visa se jedná o trojmístnou hodnotu.

### <a name="address-verification"></a>Ověření adresy

Informace z ověření adresy jsou vždy odeslány poskytovateli plateb. Můžete se rozhodnout, kolik informací je požadován pro transakce, které mají být přijaty. Ujistěte se, obraťte se na svého poskytovatele, zda přijímá tyto informace. Máte tyto možnosti k ověření adresy:
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
Pokud dodáváte část objednávky, je zachycen výši částečné objednávky a povolení, která byla přenášena celou objednávku, je uzavřen. Nové povolení podána poté pro zbývající částka objednávky, které nebylo dodáno.

## <a name="voiding-an-authorization"></a>Anulování autorizace 
Pro anulování autorizace platební karty můžete změnit metodu platby na jinou metodu, která nemá typ Platební karta.






