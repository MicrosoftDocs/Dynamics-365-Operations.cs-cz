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
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441091"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="7c9d3-103">Ověření vlastního certifikátu NF-e</span><span class="sxs-lookup"><span data-stu-id="7c9d3-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c9d3-104">Když zapnete funkci ověření vlastního certifikátu NF-e, umožní se připojení k webovým službám.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="7c9d3-105">Toto připojení je vyžadováno pro přenos NF-e a přijímání povolení ze SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="7c9d3-106">Vlastnost **Účel ověření serveru** z certifikátu V5 vydává brazilská autorita pro kořenové certifikáty.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="7c9d3-107">Tato vlastnost je ve výchozím nastavení vypnutá a je třeba ji povolit ručně.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="7c9d3-108">Za určitých okolností může automatická aktualizace certifikátu tuto vlastnost přepnout tak, že už nebude povolena.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="7c9d3-109">Pokud k tomu dojde, bude ovlivněno připojení TLS a už nebude důvěryhodné.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="7c9d3-110">Je také ovlivněna schopnost vydávat NF-e v produkčním prostředí pro státy Minas Gerais (MG) a Paraná (PR).</span><span class="sxs-lookup"><span data-stu-id="7c9d3-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="7c9d3-111">Tato aktualizace umožňuje alternativní řešení ověření certifikátu, což znamená, že je možné navázat zabezpečenou komunikaci.</span><span class="sxs-lookup"><span data-stu-id="7c9d3-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


