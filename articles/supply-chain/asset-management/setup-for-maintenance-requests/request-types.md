---
title: Typy požadavků na údržbu
description: Toto téma vysvětluje, jak nastavit stavy životního cyklu požadavků na údržbu v modulu Správa majetku.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ff80b2f3e23f46467b8a2fe7a2abd805e5e3a20
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808489"
---
# <a name="maintenance-request-types"></a>Typy požadavků na údržbu

[!include [banner](../../includes/banner.md)]

 

Typy požadavků údržby slouží ke kategorizaci požadavků na údržbu. Můžete mít například typy požadavků na údržbu, které souvisejí s preventivní údržbou a opravnou údržbou. Nebo můžete mít speciální typ požadavku na údržbu, který se používá ke správě opravy majetku (oprava skladu).

Typ požadavku údržby definuje příslušnost ke skupině stavů životního cyklu požadavků na údržbu (model životního cyklu údržby). Modely životního cyklu požadavků údržby definují stavy životního cyklu, které lze nastavit pro požadavek údržby. (Příklady stavů životního cyklu požadavků na údržbu zahrnují **Vytvořené** **Aktivní** a **Ukončené**.)

1. Vyberte **Správa majetku** \> **Nastavení** \> **Požadavky na údržbu** \> **Typy požadavků na údržbu**.
2. Zvolte **Nový** pro vytvoření typu životního cyklu požadavku na údržbu.
3. V poli **Typy požadavků na údržbu** zadejte ID pro typ požadavku údržby.
4. Do pole **Název** zadejte název.
5. Na kartě **Obecné** v poli **Model životního cyklu požadavků údržby** vyberte model životního cyklu požadavků údržby.
6. V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu. Když je požadavek na údržbu převeden na pracovní příkaz, pracovní příkaz automaticky získá typ pracovního příkazu, který souvisí s typem požadavku údržby.

Následující ilustrace znázorňuje příklad stránky **Typy požadavků na údržbu**.

![Stránka Typy požadavků na údržbu](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]