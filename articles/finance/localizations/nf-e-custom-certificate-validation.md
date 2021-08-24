---
title: Ověření vlastního certifikátu NF-e
description: Toto téma přináší informace o povolení a používání vlastního certifikátu NF-e.
author: gionoder
ms.date: 07/29/2021
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755584"
---
# <a name="nf-e-custom-certificate-validation"></a>Ověření vlastního certifikátu NF-e

[!include [banner](../includes/banner.md)]

Vlastnost **Účel ověření serveru** z certifikátů vydaných Brazilian Root Certificate Authority je ve výchozím nastavení vypnutá a musí být povolena ručně. Za určitých okolností může automatická aktualizace certifikátu tuto vlastnost přepnout tak, že už nebude povolena. Pokud k tomu dojde, bude ovlivněno připojení TLS a už nebude důvěryhodné. Je také ovlivněna schopnost vydávat model brazilského elektronického fiskálního dokumentu 55 pro státy Minas Gerais (MG) a Paraná (PR).

Chcete -li povolit opravu pro **Ověření vlastního certifikátu NF-e**, přejděte do **Správy funkcí**. Tato funkce umožňuje alternativní řešení ověřování certifikátů V5 a V10 a umožňuje důvěryhodné spojení s webovými službami, které je nutné pro bezpečný přenos NF-e a přijetí autorizace od SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
