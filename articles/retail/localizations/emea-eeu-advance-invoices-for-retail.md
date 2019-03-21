---
title: Zálohové faktury pro Retail pro východní Evropu
description: Toto téma vysvětluje, jak nastavit oznámení zálohách v maloobchodu pro východní Evropu.
author: epopov
manager: annbe
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0dd49d6fc3294342ebc13d16eb871d0b20229b0c
ms.sourcegitcommit: 2cf5498098e7a5ade1c16eac6df26bc98e4565cd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2019
ms.locfileid: "760700"
---
# <a name="advance-invoices-for-retail-for-eastern-europe"></a>Zálohové faktury pro Retail pro východní Evropu

[!include [banner](../includes/banner.md)]

Informace v tomto tématu platí pro východoevropskou lokalizaci a souvisí s maloobchodem.

Pro Polsko, Maďarsko a Českou republiku platí, že při přijetí zálohy od odběratele pomocí pokladního místa (POS), musí být záloha zaregistrována pro daňové účely a musí být generován a vytištěn zálohový doklad obsahující částku zálohové faktury. Kromě toho pro Polsko platí, že musí být transakce zálohové faktury zaúčtovány v hlavní knize.

Po konečném zaúčtování faktury faktury prodejní objednávky by měl konečný doklad obsahovat zálohovou fakturu a měly by být uvedeny všechny zálohy.

Pokud prodejní objednávky generujete z modulu Pohledávky, musíte ručně generovat zálohové faktury pomocí kroků uvedených v části [Zálohové faktury pro východní Evropu](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice). Pokud generujete prodejní objednávky prostřednictvím POS systém vytvoří a zaúčtuje zálohové faktury za vás.

## <a name="supported-scenarios"></a>Podporované scénáře

Podporovány jsou následující scénáře:

- Vytvořte a zaúčtujte zálohovou fakturu.
- Změňte částku vkladu. Pokud se zákazník rozhodne zvýšit výši vkladu, bude vystavena další zálohová faktura. Pro všechny ostatní změny částky vkladu (pokud je například zakázka odběratele upravena) je vytvořen dobropis pro zálohovou fakturu, která již byla vygenerována a je generována a zaúčtována nová zálohová faktura pro opravenou částku.
- Zrušte prodejní objednávku, ke které jsou připojené zálohové faktury. V takovém případě je vytvořen dobropis zálohové faktury.
- Zaúčtujte fakturu prodejní objednávky, ke které jsou připojené zálohové faktury. Zálohová faktura, která je spojena s prodejní objednávkou, je stornována na množství na prodejní faktuře. Transakce zálohové faktury jsou vypořádány s transakcemi storna zálohové faktury.

## <a name="set-up-advance-invoices"></a>Nastavení zálohových faktur

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a>Zapnutí funkce vytváření zálohových faktur

1. Přejděte na možnost **Maloobchod \> Nastavení centrály \> Parametry \> Parametry maloobchodu**.
2. Na kartě **Objednávky odběratele** na pevné záložce **Objednávka** nastavte možnost **Vytvořit zálohovou fakturu pro vklad** na **Ano**.

### <a name="define-the-parameters-for-posting-advance-invoices"></a>Definování parametrů zaúčtování zálohových faktur

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
2. Na kartě **Aktualizace** na pevné záložce **Zálohová faktura** nastavte pole **Profil zaúčtování**, **Skupina daně z prodeje** a **Skupina daně z prodeje** položky. Pokud jsou tato pole nastavena správně, zálohová faktura se zaúčtuje. Jestliže tato pole nejsou nastavena, faktury nebudou zaúčtovány.

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a>Vypnutí zaúčtování DPH na zálohovém dokladu deníku

Pokud je zapnuto zaúčtování zálohových faktur, nesmí být zaúčtována DPH na zálohovém dokladu deníku. Chcete-li ověřit, že tento požadavek je splněn, postupujte takto.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
2. Na kartě **Hlavní kniha a DPH** se na pevné záložce **Platba** ujistěte, že jsou následující pole prázdná nebo nastavená na **Ne**:

    - DPH na zálohovém dokladu deníku
    - Účetní profil se zálohovým dokladem deníku
    - Skupina daně pro zálohy
    - Skupina DPH u položky

## <a name="print-advance-invoices"></a>Tisk zálohových faktur

Zálohové faktury můžete tisknout z POS na tiskárně Microsoft Windows, která je připojena k hardwarové stanici. Existují dvě možnosti tisku zálohové faktury z POS:

- **Tisk zálohové faktury po uzavření transakce v POS.** Tato možnost se objeví automaticky, pokud byla vygenerovaná zálohová faktura a správně nastavena tiskárna systému Windows. V takovém případě se vytiskne pouze poslední zálohová faktura, která je propojena s objednávkou odběratele.
- **Znovu vytisknout zálohovou fakturu z deníku transakce.** Vyberte **zobrazit deník** pro otevření deníku transakcí, vyhledejte objednávku odběratele a poté vyberte **Tisk zálohové faktury**. V takovém případě se vytisknou všechny zálohové faktury, které jsou propojeny s objednávkou odběratele.

### <a name="set-up-a-windows-printer"></a>Nastavení tiskárny Windows

Tento postup slouží k povolení tisku dokumentů z POS na tiskárně Windows, která je připojena k hardwarové stanici dokumentů.

1. Přejděte na **Maloobchod \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**.
2. Vyberte hardwarový profil vztahující se k obchodu, kde se používá tiskárna.
3. Aktualizujte nastavení v části **Tiskárna** nebo **Tiskárna 2**:

    - V polo **Tiskárna** vyberte **Ovladač systému Windows**.
    - Do pole **Název zařízení** zadejte název tiskárny.

4. Přejděte do nabídky **Maloobchodní prodej \> Maloobchodní IT \> Distribuční plán**.
5. Vyberte úlohu **1090** a klikněte na tlačítko **Spustit**.
