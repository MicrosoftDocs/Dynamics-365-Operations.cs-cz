---
title: Tisk informací o dani na dokumentech převodního příkazu
description: Toto téma vysvětluje, jak lze daňové informace určené službou výpočtu daně vytisknout na dokumenty převodního příkazu.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e74336270ab46fc19adb4c797745c9582028391a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687464"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Tisk informací o dani na dokumentech převodního příkazu

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytisknout informace o dani na dokumentech převodního příkazu. Můžete vytisknout doklad proforma faktury převodního příkazu pro skladové převody, které jsou považovány za dodání uvnitř Společenství a pořízení uvnitř Společenství podle předpisů Evropské unie (EU) o dani z přidané hodnoty (DPH). 

Do dokladů převodního příkazu jsou doplněny následující daňově relevantní údaje:

- Jména a adresy odesílatele a příjemce pro převod zásob
- Daňová identifikační čísla dodavatele a příjemce
- Jednotková cena a základ daně dodávaného zboží
- Daňový řád, sazba daně, výše daně a daňové směrnice

Chcete-li nakonfigurovat tato data, musíte provést následující hlavní kroky.

1. [Povolte a nastavte daňovou funkci pro převodní příkazy](tasks/Tax-feature-support-for-transfer-order.md).
2. [Vytvořte a nastavte více daňových registračních čísel pro právnickou osobu](emea-multiple-vat-registration-numbers.md).
3. Nastavte kód osvobození, popis, daňové směrnice a tiskový kód v daňových kódech. V tomto příkladu jsou vytvořeny tři daňové kódy a synchronizováno do Microsoft Dynamics 365 Finance: **NL-Exempt**, **BE-RC-21** a **BE-RC+21**.

    1. Ve Finance přejděte do nabídky **Daň** \> **Nastavení** \> **DPH** \> **Kódy osvobození DPH**.
    2. Vyberte **Upravit** a zadejte popis pro kód osvobození **ES**. Například zadejte **Zásilky ES osvobozené od daně s daňovým registračním číslem**.
    3. Přejděte k nabídce **Daň** \> **Nepřímé daně** \> **DPH** \> **Kódy DPH**.
    4. Vyberte daňový kód **BE-RC-21** a poté vyberte **Daňové směrnice**.
    5. Zvolte **Nové**.
    6. V poli **Jazyk** vyberte **EN-US**. Poté v poli **Text** zadejte **Dokument stanovující převod zboží ve smyslu čl. 138 odst. 2 písm. c) směrnice EU o DPH 2006/112/ES**.
    7. Zavřete stránku.
    8. Na pevné záložce **Všeobecné** v poli **Tisk** vyberte **Sazba DPH**.
    8. Vyberte daňový kód **NL-Exempt** a poté na pevné záložce **Všeobecné** v poli **Tisk** vyberte **Sazba DPH**.

    > [!NOTE] 
    > Kód daně, sazba daně a popis osvobození od daně se na dokumentech převodního příkazu nevytisknou, pokud pro daňový kód není zachován popis kódu osvobození od daně nebo daňové směrnice.

## <a name="print-the-transfer-order---shipment-document"></a>Tisk převodního příkazu – dokladu o odeslání

Po odeslání převodu vytiskněte převodní příkaz – dokument o odeslání podle následujících kroků.

1. Přejděte na **Řízení zásob** \> **Dotazy a zprávy** \> **Převodní příkazy** \> **Dodávka**.
2. Na kartě **Parametry** ve skupině **Tisk** aktivujte **Daňové informace**.
3. Na kartě **Záznamy k zahrnutí** vyberte **Filtr**, vyberte číslo převodní objednávky a poté vyberte **OK**.
4. Vybere **OK** pro tisk převodního příkazu – dokladu o odeslání.

## <a name="print-the-transfer-order---receipt-document"></a>Tisk převodního příkazu – dokladu o příjmu

Po příjmu převodu vytiskněte převodní příkaz – dokument o příjmu podle následujících kroků.

1. Přejděte na **Řízení zásob** \> **Dotazy a zprávy** \> **Převodní příkazy** \> **Příjem**.
2. Na kartě **Parametry** ve skupině **Tisk** aktivujte **Daňové informace**.
3. Na kartě **Záznamy k zahrnutí** vyberte **Filtr**, vyberte číslo převodní objednávky a poté vyberte **OK**.
4. Vybere **OK** pro tisk převodního příkazu – dokladu o příjmu.

## <a name="print-the-transfer-overview-document"></a>Tisk dokumentu s přehledem převodu

Chcete-li vytisknout dokument s přehledem převodu, postupujte podle těchto kroků.

> [!NOTE]
> Daňové informace jsou dostupné pouze tehdy, když byl převodní příkaz odeslán nebo přijat.

1. Přejděte na **Řízení zásob** \> **Dotazy a zprávy** \> **Převodní příkazy** \> **Přehled převodu**.
2. Na kartě **Parametry** ve skupině **Tisk** aktivujte **Daňové informace**.
3. Na kartě **Záznamy k zahrnutí** vyberte **Filtr**, vyberte číslo převodní objednávky a poté vyberte **OK**.
4. Vybere **OK** pro tisk dokladu s přehledem převodu.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
