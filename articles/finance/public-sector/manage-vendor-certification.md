---
title: Správa certifikace dodavatele
description: Tento článek popisuje kroky, které mohou dodavatelé použít ke správě svých certifikací pomocí pracovního prostoru Spolupráce s dodavateli.
author: TaylorVH
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c66952d19cddd9d4a9a102ba59e8d6d97b75ed4d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2022
ms.locfileid: "9583198"
---
# <a name="maintain-vendor-certification"></a>Správa certifikace dodavatele

[!include [banner](../includes/banner.md)]

Tento článek popisuje kroky, které můžete použít ke správě svých certifikací pomocí pracovního prostoru **Spolupráce s dodavateli**. Příklady certifikací mohou zahrnovat společnost Woman Business Enterprise (WBE) nebo společnost Leadership in Energy and Environment Design (LEED). Dodavatelé budou muset zadat informace o certifikaci do pracovního prostoru **Informace o dodavateli**. Odtud vyberou **Více informací** a poté **Certifikace**.

## <a name="turn-on-the-vendor-certification-feature"></a>Zapnutí funkce certifikace dodavatele

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí stránky [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul** - *Závazky*
- **Název funkce** - *Povolit správu certifikace dodavatelské spolupráce*

## <a name="add-a-new-certification"></a>Přidání nové certifikace

Chcete-li přidat novou certifikaci, vyberte tlačítko **Přidat**, které je umístěno nad mřížkou **Osvědčení** v pracovním prostoru **Informace o prodejci**. Zadejte následující informace:

- Číslo certifikátu
- Typ certifikátu
- Certifikační organizace
- Datum certifikátu
- Částka závazku, pokud existuje
- Platný od
- Datum konce platnosti
- Komentáře, nepovinné

Pokud existují dokumenty týkající se konkrétní certifikace, můžete je přiložit pomocí tlačítka **Dokument**.

Certifikacím, které zadávají vaši prodejci na této stránce, bude přiřazen zdroj „Dodavatel“. Informace o certifikátu můžete zadat jménem dodavatele na bankovních účtech dodavatele. Informace se zobrazí zde a zdroj se zobrazí jako **Zákazník**.

Prodejci mohou podle potřeby upravit nebo odstranit své certifikace.

## <a name="vendor-collaboration-generated-certification-records"></a>Spolupráce s dodavateli generuje záznamy o certifikaci

Poté, co dodavatel přidá informace o certifikaci, budou tyto informace viditelné na stránce **Certifikace generované spoluprací s dodavateli**. Chcete-li stránku otevřít, přejděte na **Závazky > Dotazy> Zprávy dodavatele> Certifikace generované spoluprací s dodavateli**. Ve výchozím nastavení jsou viditelné všechny nové nebo upravené záznamy o certifikaci. Závazkový úředník si může prohlédnout změny a ověřit informace prostřednictvím procesu potvrzení, aby je ověřil. Po potvrzení informací lze vybrat certifikační záznam uvedený na stránce a označit jej jako zkontrolovaný. Označením záznamu jako zkontrolovaného jej odstraníte z výchozího seznamu.

Všechny změny certifikace jsou viditelné na stránce **Certifikace generované spoluprací s dodavateli**. Pokud se změna na stránce nezobrazí, můžete ji zobrazit úpravou filtrů pro účet dodavatele, rozsahu účinných dat nebo volbou, zda chcete zahrnout informace o změnách certifikace, které byly zkontrolovány.

