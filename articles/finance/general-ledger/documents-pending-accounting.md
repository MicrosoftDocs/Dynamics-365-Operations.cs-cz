---
title: Dokumenty čekající na účetnictví
description: Tento článek popisuje, jak používat funkce na stránce Dokumenty čekající na účetnictví.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: e915c248abd1c842f8f01490a49db9b824644a29
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9424359"
---
# <a name="documents-pending-accounting"></a>Dokumenty čekající na účetnictví

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tento článek popisuje, jak používat funkce na stránce **Dokumenty čekající na účetnictví**.

V aplikaci Microsoft Dynamics 365 Finance 10.0.30 je k dispozici funkce **Vylepšený výkon pro architekturu účetnictví zdrojových dokumentů**. Tato funkce zlepšuje procesy zaúčtování pro zaúčtování dokumentů se zdrojovými dokumenty, počínaje procesem zaúčtování faktur s volným textem.

Pokud je tato funkce povolena, zaúčtování dokumentu dílčí hlavní knihy se provádí odděleně od procesu generování účetnictví nebo *zápisu do deníku*, který vytváří úplný účetní detail přenášený do hlavní knihy. Například v procesu zaúčtování faktury s volným textem je faktura zákazníka v modulu **Pohledávky** zaznamenána dříve, než je vytvořeno úplné účetnictví. Tato funkce pro zvýšení výkonu umožňuje rychlejší zaúčtování faktur zákazníkům při zpožděném generování účetnictví.

Na stránce **Dokumenty čekající na účetnictví** jsou k dispozici následující tlačítka.

- **Generovat účetnictví** – Odeslání dokumentu, který právě čeká na vygenerování účtu pro zápis do deníku.
- **Zobrazit rozúčtování** – Zobrazení rozúčtování pro vybraný dokument v seznamu.
- **Zobrazit protokol chyb** – Zobrazení všech podrobností o chybových zprávách, které existují pro dokument, u něhož stav účetnictví uvádí chyby. Stejné podrobnosti o chybové zprávě můžete zobrazit výběrem odkazu **Protokol chyb** na řádku dokumentu.

Generování účetnictví je prováděno procesem automatizace procesu na pozadí, který se nazývá **Procesor architektury účetnictví**. Další informace o nastavení a konfiguraci všech automatizací procesů naleznete v části [Automatizace procesů](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
