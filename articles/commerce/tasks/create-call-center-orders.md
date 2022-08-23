---
title: " Vytváření objednávek v kontaktním středisku"
description: Tento článek vás provede příkladem postupu, kdy uživatel call centra vyhledá zákazníka, vytvoří novou objednávku, vyhledá produkt a inkasuje platbu od zákazníka v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228503"
---
# <a name="create-call-center-orders"></a> Vytváření objednávek v kontaktním středisku

[!include [banner](../includes/banner.md)]

Tento článek vás provede příkladem postupu, kdy uživatel call centra vyhledá zákazníka, vytvoří novou objednávku, vyhledá produkt a inkasuje platbu od zákazníka v Microsoft Dynamics 365 Commerce. Postup používá ukázková data USRT společnosti a je určena pro úředníka prodejní objednávky. 

## <a name="prerequisites"></a>Předpoklady

Uživatel, který postup provádí, musí být nastaven jako uživatel call centra. Volitelně lze publikovat pololetní katalog Fabrikam s alespoň jedním zdrojovým kódem.

### <a name="add-yourself-as-a-call-center-user"></a>Přidání se jako uživatele call centra

Chcete-li se přidat jako uživatel call centra, postupujte takto:

1. V Commerce Headquarters přejděte na možnost **Retail a Commerce \> Kanály \> Call centra \> Všechna call centra**.
1. V poli **Uživatelé** vyberte **Uživatelé kanálu**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **ID uživatele** zadejte vaše ID uživatele.
1. Do pole **Název** zadejte své uživatelské jméno. Uživatelské jméno může být stejné jako ID uživatele.
1. V podokně akcí vyberte **Uložit**.
1. Vraťte se na **Retail a Commerce \> Kanály \> Call centra \> Všechna call centra**.
1. Vyberte ID maloobchodního kanálu call centra.
1. Potvrďte, že možnost **Povolit provedení objednávky** je nastavena na **Ano**. Pokud možnost není viditelná, můžete tento krok přeskočit.

## <a name="complete-the-example-call-center-procedure"></a>Provedení ukázkového postupu call centra

Chcete-li provést ukázkový postup call centra, postupujte takto.

1. Přejděte na **Retail a Commerce \> Odběratelé \> Služby odběratele**.
1. Na kartě **Hledání zákazníka** zadejte kritéria vyhledávání pro vyhledávání zákazníka. Pro tuto vzorovou proceduru **Karen**.
1. Vyberte **Vyhledat**. Zobrazí se dialogové okno **Vyhledávání zákazníků** se seznamem výsledků hledání.
1. Vyberte záznam zákazníka pro **Karen Berg**, který má číslo zákaznického účtu **2001**, a poté vyberte **Vybrat**.
1. V podokně akcí zvolte **Nová prodejní objednávka**.
1. Vpravo vyberte kartu **Záhlaví**.
1. Na záložce s náhledem **Doručení** v poli **Režim doručení** vyberte **99 standardní**.

    ![Výběr způsobu dodání.](../media/Select_Mode_of_Delivery.png)

1. Vpravo vyberte kartu **Řádky**.
1. V části **Řádky prodejní objednávky** na novém řádku pro nový prodejní řádek do pole **Číslo položky** zadejte číslo položky, kterou chcete vyhledat. Pro tento příklad postupu zadejte **81327** a poté vyberte produkt z rozevíracího seznamu a přidejte ho do prodejní objednávky.
1. Do pole **Množství** zadejte množství prodeje.
1. V poli **Zdrojový kód** vyberte zdrojový kód katalogu. Pokud neexistují žádné aktivní zdrojové kódy, můžete tento krok vynechat.
1. V podokně akcí výběrem **Dokončit** zachytíte platbu odběratele. Tato akce otevře dialogové okno **Shrnutí prodejní objednávky**, které zobrazuje celkovou splatnou částku. Tato akce také spustí výpočet jakýchkoli poplatků, jako je doprava a manipulace, a zobrazí je v dialogovém okně **Shrnutí prodejní objednávky**.

    ![Tlačítko Dokončit.](../media/Complete_button.png)

1. V dialogovém okně **Shrnutí prodejní objednávky** na pevné záložce **Platby** vyberte **Přidat** k zachycení plateb.

    ![Souhrnné dialogové okno prodejní objednávky.](../media/order_summary.png)

1. V dialogovém okně **Zadat platební údaje zákazníka** v poli **Způsob platby** vyberte způsob platby. Pro tuto vzorovou proceduru vyberte **Hotovost**.
1. V poli **Částka platby** zadejte částku platby. Pro tento příklad zadejte **120,00**, což se rovná zůstatku objednávky, který je uveden v dialogové okně **Shrnutí prodejní objednávky**. Zadáním této částky budete moci ukončit objednávku jako plně zaplacenou.
1. Vyberte **OK**.
1. Vyberte **Odeslat**.

## <a name="additional-resources"></a>Další prostředky

[Přizpůsobení transakčních e-mailů podle způsobu doručení](../customize-email-delivery-mode.md)

[Změna způsobu dodání v POS](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
