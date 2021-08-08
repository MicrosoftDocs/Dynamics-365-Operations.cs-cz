---
title: Použití externích dat v prognózách peněžních toků (náhled)
description: Toto téma popisuje kroky nastavení, které musíte provést, aby bylo možné do prognóz peněžních toků zadávat nebo importovat externí data.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b728314f4c4e18543e4f3b75fe1e7dcddc448ea0
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638529"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Použití externích dat v prognózách peněžních toků (náhled)

[!include [banner](../includes/banner.md)]

Externí data lze zadávat nebo importovat do prognóz peněžních toků. Toto téma popisuje kroky nastavení, které jsou specifické pro použití externích dat a které umožňují zahrnutí externích dat do prognózy peněžních toků.

## <a name="external-data-setup"></a>Nastavení externích dat

Použijte kartu **Vnější zdroj** na stránce **Nastavení předpovědi peněžních toků** (**Pokladna a banka \> Prognóza peněžních toků**) a zadejte nastavení, která podporují použití externích dat v předpovědích peněžních toků.

Další informace o nastavení čítačů naleznete v tématu [Prognóza cashflow](../cash-bank-management/cash-flow-forecasting.md).

Chcete-li zadat externí data pro prognózy peněžních toků, můžete k zadávání a úpravě externích dat použít prostředí Otevřít v aplikaci Excel. Vyberte tlačítko **Externí data** a poté vyberte **Přidat externí data** nebo **Upravit existující externí data**. Když je soubor Microsoft Excel otevřen, můžete zadat informace do následujících polí:

- **ID položky**
- **Popis** (nepovinné)
- **Název externího zdroje** - Vyberte jednu z hodnot v seznamu, který jste definovali při nastavování nástroje Finanční přehledy.
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
