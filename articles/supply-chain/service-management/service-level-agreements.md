---
title: Přehled smluv o úrovni služeb
description: Ve smlouvě SLA odběratel souhlasí s minimálním časem odezvy od okamžiku, kdy servisní společnost zaznamená problém, do okamžiku vyřešení potíží.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2cfa8b72e515b6237914499af626ff8262429d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974353"
---
# <a name="service-level-agreements-overview"></a>Přehled smluv o úrovni služeb       

[!include [banner](../includes/banner.md)]


Smlouva o úrovni služeb (SLA) představuje dohodu mezi servisní společností a odběratelem služeb. Ve smlouvě SLA odběratel souhlasí s minimálním časem odezvy od okamžiku, kdy servisní společnost zaznamená problém, do okamžiku vyřešení potíží.

Smlouva SLA zaručuje standardní úroveň služeb, které jsou nabízeny zákazníkům, a také pro servisní společnost jasně definuje čas, za který musí být servisní zákrok dokončený.

Odběratelům služeb lze nabídnout různé úrovně služeb, pro které lze vytvořit různé smlouvy SLA.

## <a name="create-a-service-level-agreement"></a>Vytvoření smlouvy o úrovni služeb (SLA)

1.  Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Smlouva o úrovni služeb**.

2.  Zadejte název smlouvy o úrovni služeb do pole **Smlouva o úrovni služeb**.

3.  Zadejte čas, který chcete povolit pro dokončení servisních volání, která jsou připojena ke smlouvě o úrovni služeb. Poté vyberte kalendář, pokud chcete založit smlouvu o úrovni služeb na konkrétním kalendáři.

## <a name="apply-a-service-level-agreement"></a>Použití smlouvy o úrovni služeb (SLA)

Smlouva SLA se použije přímo na servisní smlouvu.

Servisní zakázky, které vytvoříte ručně a připojíte k servisní smlouvě se smlouvou SLA, jsou kontrolovány proti této smlouvě SLA.

Servisní zakázky, které jsou vytvořeny automaticky, nejsou připojeny ke smlouvě SLA.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Použití smlouvy o úrovni služeb na servisní smlouvu

1.  Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**. Vyberte servisní smlouvu, pro kterou chcete použít SLA, a klepněte na tlačítko **upravit** v **podokně akcí**.

2.  V poli **smlouva o úrovni služeb** vyberte smlouvy o úrovni služeb, které chcete přiřadit.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Použití smlouvy o úrovni služeb na skupinu servisních smluv

1.  Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Skupiny servisních smluv**.

2.  V poli **smlouva o úrovni služeb** vyberte smlouvy o úrovni služeb, které chcete přiřadit.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Sledování času v servisní smlouvě v porovnání se smlouvou SLA

Při vytváření nové servisní zakázky pro servisní smlouvy, které je přiřazena SLA, může být aktivován časový interval pro dodání služby a systém začne sledovat čas dodání. Navíc můžete nastavit následující možnosti:

  - Sledování času pro servisní zakázky lze spouštět a zastavovat a sledovat celkový čas strávených na servisních zakázkách.

  - Můžete kontrolovat dodržování dohodnutého časového intervalu odezvy, který je určený ve smlouvě o úrovni služeb.

  - Můžete definovat kódy rozhodnutí, které je nutné nastavit při překročení časového intervalu určeného smlouvou SLA.

## <a name="see-also"></a>Viz také

[Zobrazení shody se smlouvou na úrovni služeb](view-compliance-with-service-level-agreements.md)

  


