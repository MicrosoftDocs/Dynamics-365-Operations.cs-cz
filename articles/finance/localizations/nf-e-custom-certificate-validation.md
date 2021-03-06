---
title: Ověření vlastního certifikátu NF-e
description: Toto téma přináší informace o povolení a používání vlastního certifikátu NF-e.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813961"
---
# <a name="nf-e-custom-certificate-validation"></a>Ověření vlastního certifikátu NF-e

[!include [banner](../includes/banner.md)]

Když zapnete funkci ověření vlastního certifikátu NF-e, umožní se připojení k webovým službám. Toto připojení je vyžadováno pro přenos NF-e a přijímání povolení ze SEFAZ.

Vlastnost **Účel ověření serveru** z certifikátu V5 vydává brazilská autorita pro kořenové certifikáty. Tato vlastnost je ve výchozím nastavení vypnutá a je třeba ji povolit ručně. Za určitých okolností může automatická aktualizace certifikátu tuto vlastnost přepnout tak, že už nebude povolena. Pokud k tomu dojde, bude ovlivněno připojení TLS a už nebude důvěryhodné. Je také ovlivněna schopnost vydávat NF-e v produkčním prostředí pro státy Minas Gerais (MG) a Paraná (PR).

Tato aktualizace umožňuje alternativní řešení ověření certifikátu, což znamená, že je možné navázat zabezpečenou komunikaci.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]