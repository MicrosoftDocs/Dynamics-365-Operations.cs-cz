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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240572"
---
# <a name="nf-e-custom-certificate-validation"></a>Ověření vlastního certifikátu NF-e

[!include [banner](../includes/banner.md)]

Když zapnete funkci ověření vlastního certifikátu NF-e, umožní se připojení k webovým službám. Toto připojení je vyžadováno pro přenos NF-e a přijímání povolení ze SEFAZ.

Vlastnost **Účel ověření serveru** z certifikátu V5 vydává brazilská autorita pro kořenové certifikáty. Tato vlastnost je ve výchozím nastavení vypnutá a je třeba ji povolit ručně. Za určitých okolností může automatická aktualizace certifikátu tuto vlastnost přepnout tak, že už nebude povolena. Pokud k tomu dojde, bude ovlivněno připojení TLS a už nebude důvěryhodné. Je také ovlivněna schopnost vydávat NF-e v produkčním prostředí pro státy Minas Gerais (MG) a Paraná (PR).

Tato aktualizace umožňuje alternativní řešení ověření certifikátu, což znamená, že je možné navázat zabezpečenou komunikaci.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]