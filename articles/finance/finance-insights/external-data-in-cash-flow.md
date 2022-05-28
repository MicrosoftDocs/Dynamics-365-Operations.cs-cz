---
title: Externí data v prognózách cashflow
description: Toto téma popisuje kroky nastavení, které musíte provést, aby bylo možné do prognóz peněžních toků zadávat nebo importovat externí data.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f7fac80b7ad0fde273fbd33aa5df146e569be46e
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713719"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Externí data v prognózách cashflow

[!include [banner](../includes/banner.md)]

Externí data lze zadávat nebo importovat do prognóz peněžních toků. Toto téma popisuje kroky nastavení, které jsou specifické pro použití externích dat a které umožňují zahrnutí externích dat do prognózy peněžních toků.

## <a name="external-data-setup"></a>Nastavení externích dat

Použijte kartu **Vnější zdroj** na stránce **Nastavení předpovědi cashflo** (**Pokladna a banka \> Prognóza cashflow \> Nastavení prognózy cashflow**) a zadejte nastavení, která podporují použití externích dat v předpovědích cashflow.

Externí data lze zadávat nebo importovat do prognóz peněžních toků. Před zadáním nebo importem externích dat je třeba nastavit externí zdroje. Na kartě **Vnější zdroj** nastavte externí kategorie peněžních toků. Kategorie může být buď **Odchozí** nebo **Příchozí**. **Likvidita** by měla být vybrána jako typ účtování. V mřížce **Nastavení právnické osoby** vyberte právnické osoby a odpovídající hlavní účty, na které se vztahují kategorie externích peněžních toků.

Další informace o nastavení prognóz cashflow naleznete v tématu [Prognóza cashflow](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Vložte externí data

Chcete-li zadat a upravovat externí data pro prognózy peněžních toků, můžete použít prostředí **Otevřít v aplikaci Excel**. Vyberte tlačítko **Externí data** na stránce pracovního prostoru **Nastavení prognózy cashflow** a poté vyberte **Přidat externí data** nebo **Upravit existující externí data**. Když je soubor Microsoft Excel otevřen, můžete zadat informace do následujících polí:

- **ID položky** (jedinečné)
- **Popis** (nepovinné)
- **Název externího zdroje** - Vyberte jednu z hodnot v seznamu, který jste definovali při nastavování nástroje Finance Insights.
- **Právnická osoba**
- **Datum**
- **Částka v měně transakce**
- **Kód měny**
- **Výchozí dimenze** (volitelný)
- **Číslo dokumentu** (volitelný)
- **Číslo účtu** (volitelný)
- **Název účtu** (volitelný)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Import externích dat pomocí rámce Správy dat

Můžete importovat externí data pro předpovědi peněžních toků pomocí pracovního prostoru **Správa dat** a entity, která se jmenuje **Předpověď peněžního toku externího vstupu zdroje**.

Kromě toho, pokud musíte přesunout data nastavení z jednoho prostředí do jiného, je pro tyto tabulky nastavení k dispozici následující oblast entit:

- Nastavení externího zdroje prognózy cashflow
- Nastavení právnické osoby externího zdroje prognózy cashflow

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
