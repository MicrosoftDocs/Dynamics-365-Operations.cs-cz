---
title: Zpracování příchozích elektronických dokumentů
description: Toto téma poskytuje přehled zpracování příchozích elektronických dokumentů.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371537"
---
# <a name="processing-of-incoming-electronic-documents"></a>Zpracování příchozích elektronických dokumentů

[!include [banner](../includes/banner.md)]

Příchozí elektronické dokumenty, jako jsou elektronické faktury dodavatele, lze importovat a zpracovávat dvěma způsoby:

- Soubory jsou načítány z externích kanálů a předávány přímo do vaší připojené aplikace. Tam procházejí dodatečnou transformací a následně jsou importovány do databáze.
- Soubory procházejí předzpracováním ve službě Elektronická fakturace a poté jsou předány do vaší připojené aplikace.

Elektronická fakturace podporuje dva kanály pro příchozí dokumenty: e-mail a složky Microsoft SharePoint.

Existují typy nastavení twp, které určují, zda dokumenty procházejí předzpracováním, nebo jsou předány přímo vaší připojené aplikaci:

- **Datový kanál** – Systém předá dokument přímo připojené aplikaci.
- **Datový kanál s kanálem zpracování** – Můžete nastavit další akce, které budou spuštěny před předáním dokumentu do připojené aplikace.

Informace o tom, jak nastavit scénáře pro zpracování příchozích elektronických dokumentů pro různé kanály, viz [Konfigurace e-mailového kanálu](e-invoicing-configure-email.md) a [Konfigurace kanálu SharePoint](e-invoicing-configure-sharepoint-channel.md).
