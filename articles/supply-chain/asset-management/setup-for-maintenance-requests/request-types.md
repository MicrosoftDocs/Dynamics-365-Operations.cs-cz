---
title: Typy požadavků na údržbu
description: Toto téma vysvětluje, jak nastavit stavy životního cyklu požadavků na údržbu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790473"
---
# <a name="maintenance-request-types"></a>Typy požadavků na údržbu

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Typy požadavků údržby slouží ke kategorizaci požadavků na údržbu. Můžete mít například typy požadavků na údržbu, které souvisejí s preventivní údržbou a opravnou údržbou. Nebo můžete mít speciální typ požadavku na údržbu, který se používá ke správě opravy majetku (oprava skladu).

Typ požadavku údržby definuje příslušnost ke skupině stavů životního cyklu požadavků na údržbu (model životního cyklu údržby). Modely životního cyklu požadavků údržby definují stavy životního cyklu, které lze nastavit pro požadavek údržby. (Příklady stavů životního cyklu požadavků na údržbu zahrnují **Vytvořené** **Aktivní** a **Ukončené**.)

1. Vyberte **Správa majetku** \> **Nastavení** \> **Požadavky na údržbu** \> **Typy požadavků na údržbu**.
2. Zvolte **Nový** pro vytvoření typu životního cyklu požadavku na údržbu.
3. V poli **Typy požadavků na údržbu** zadejte ID pro typ požadavku údržby.
4. Do pole **Název** zadejte název.
5. Na kartě **Obecné** v poli **Model životního cyklu požadavků údržby** vyberte model životního cyklu požadavků údržby.
6. V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu. Když je požadavek na údržbu převeden na pracovní příkaz, pracovní příkaz automaticky získá typ pracovního příkazu, který souvisí s typem požadavku údržby.

Následující ilustrace znázorňuje příklad stránky **Typy požadavků na údržbu**.

![Obrázek č. 1](media/07-setup-for-requests.png)
