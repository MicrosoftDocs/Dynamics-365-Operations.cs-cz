---
title: Ověření vlastního certifikátu NF-e
description: Toto téma přináší informace o povolení a používání vlastního certifikátu NF-e.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990079"
---
# <a name="nf-e-custom-certificate-validation"></a>Ověření vlastního certifikátu NF-e

[!include [banner](../includes/banner.md)]

Když zapnete funkci ověření vlastního certifikátu NF-e, umožní se připojení k webovým službám. Toto připojení je vyžadováno pro přenos NF-e a přijímání povolení ze SEFAZ.

Vlastnost **Účel ověření serveru** z certifikátu V5 vydává brazilská autorita pro kořenové certifikáty. Tato vlastnost je ve výchozím nastavení vypnutá a je třeba ji povolit ručně. Za určitých okolností může automatická aktualizace certifikátu tuto vlastnost přepnout tak, že už nebude povolena. Pokud k tomu dojde, bude ovlivněno připojení TLS a už nebude důvěryhodné. Je také ovlivněna schopnost vydávat NF-e v produkčním prostředí pro státy Minas Gerais (MG) a Paraná (PR).

Tato aktualizace umožňuje alternativní řešení ověření certifikátu, což znamená, že je možné navázat zabezpečenou komunikaci.


