---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (červenec 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: andreabichsel
manager: AnnBe
ms.date: 07/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2018-07-31
ms.dyn365.ops.version: Talent July 2018 update
ms.openlocfilehash: 5538aef6599eeffee6d9b075f1b9630d55cf982a
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812711"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-july-2018"></a><span data-ttu-id="98282-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent - Core HR (červenec 2018)</span><span class="sxs-lookup"><span data-stu-id="98282-103">What's new or changed in Dynamics 365 Talent - Core HR (July 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98282-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="98282-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="power-apps-personalization"></a><span data-ttu-id="98282-105">Individuální nastavení Power Apps</span><span class="sxs-lookup"><span data-stu-id="98282-105">Power Apps personalization</span></span>

<span data-ttu-id="98282-106">Aplikace Talent podporuje integraci se službou Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="98282-106">Talent supports integration with the Microsoft Power Apps service.</span></span> <span data-ttu-id="98282-107">Power Apps umožňují vývojářům i netechnickým uživatelům vytvářet vlastní obchodní aplikace pro mobilní zařízení, tablety a web, aniž by bylo nutné psát kód.</span><span class="sxs-lookup"><span data-stu-id="98282-107">Power Apps lets both developers and non-technical users build custom business apps for mobile devices, tablets, and the web without having to write code.</span></span> <span data-ttu-id="98282-108">Aplikace, které jste vytvořili vy, vaše organizace nebo širší ekosystém pomocí Power Apps, lze poté vložit do klienta aplikace Talent, aby bylo možné vylepšit funkce produktu.</span><span class="sxs-lookup"><span data-stu-id="98282-108">Apps that you, your organization, or the broader ecosystem develop by using Power Apps can then be embedded in the Talent client to augment the product's functionality.</span></span> <span data-ttu-id="98282-109">Například může vytvořit aplikaci pro doplnění aplikace Talent s informacemi získanými z jiného systému.</span><span class="sxs-lookup"><span data-stu-id="98282-109">For example, you might build an app that supplements Talent with information that is retrieved from another system.</span></span>

<span data-ttu-id="98282-110">Další informace naleznete v tématu [Integrace aplikací Power Apps](../fin-and-ops/get-started/embed-power-apps.md).</span><span class="sxs-lookup"><span data-stu-id="98282-110">For more information, see [Embed Power Apps apps](../fin-and-ops/get-started/embed-power-apps.md).</span></span>

## <a name="ceridian-payroll-integration"></a><span data-ttu-id="98282-111">Integrace mezd s aplikací Ceridian</span><span class="sxs-lookup"><span data-stu-id="98282-111">Ceridian payroll integration</span></span>

<span data-ttu-id="98282-112">Integrace mezi aplikacemi Talent a Ceridian Dayforce je nyní k dispozici pro USA, Kanadu a Mexiko.</span><span class="sxs-lookup"><span data-stu-id="98282-112">Integration between Talent and Ceridian Dayforce is now available for the US, Canada, and Mexico.</span></span> <span data-ttu-id="98282-113">Integrace používá rozsáhlé kategorie dat.</span><span class="sxs-lookup"><span data-stu-id="98282-113">The integration uses broad categories of data.</span></span> <span data-ttu-id="98282-114">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="98282-114">Here are some examples:</span></span>

- <span data-ttu-id="98282-115">Data lidských zdrojů</span><span class="sxs-lookup"><span data-stu-id="98282-115">Human resources data</span></span>
- <span data-ttu-id="98282-116">Data kompenzací</span><span class="sxs-lookup"><span data-stu-id="98282-116">Compensation data</span></span>
- <span data-ttu-id="98282-117">Mzdová data, jako například mzdové cykly, mzdová období a kódy příjmů</span><span class="sxs-lookup"><span data-stu-id="98282-117">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="98282-118">Data pracovníka</span><span class="sxs-lookup"><span data-stu-id="98282-118">Worker data</span></span>

<span data-ttu-id="98282-119">Další informace získáte v části [Konfigurace integrace mezd mezi aplikacemi Talent a Dayforce](configure-payroll-integration.md).</span><span class="sxs-lookup"><span data-stu-id="98282-119">For more information, see [Configure the payroll integration between Talent and Dayforce](configure-payroll-integration.md).</span></span>

## <a name="worker-tax-regions-have-been-expanded-beyond-the-us"></a><span data-ttu-id="98282-120">Oblasti daní pracovníka byly rozšířeny mimo USA</span><span class="sxs-lookup"><span data-stu-id="98282-120">Worker tax regions have been expanded beyond the US</span></span>

<span data-ttu-id="98282-121">Byla přidána podpora pro oblasti daně mimo Spojené státy.</span><span class="sxs-lookup"><span data-stu-id="98282-121">Support has been added for tax regions outside the United States.</span></span> <span data-ttu-id="98282-122">Když jsou k pracovníkům přiřazeny oblasti daně, mohou řídit výpočty daně a lze je použít v integraci s externími mzdovými řešeními.</span><span class="sxs-lookup"><span data-stu-id="98282-122">When tax regions are assigned to workers, they can drive tax calculations and can be used in integrations with external payroll solutions.</span></span>

## <a name="the-title-field-has-been-expanded-in-talent"></a><span data-ttu-id="98282-123">Pole nadpisu bylo rozšířeno v aplikaci Talent</span><span class="sxs-lookup"><span data-stu-id="98282-123">The title field has been expanded in Talent</span></span>

<span data-ttu-id="98282-124">V této aktualizaci byly rozšířeny nadpisy.</span><span class="sxs-lookup"><span data-stu-id="98282-124">Titles have been expanded in this update.</span></span> <span data-ttu-id="98282-125">Toto pole má nyní 65 znaků.</span><span class="sxs-lookup"><span data-stu-id="98282-125">The field is now 65 characters.</span></span> <span data-ttu-id="98282-126">Tato změna je provedená všude, kde je zvolený nadpis - například u pracovníků, pozic a úloh.</span><span class="sxs-lookup"><span data-stu-id="98282-126">This change has been implemented everywhere that title is selected, such as workers, positions, and jobs.</span></span>

## <a name="benefit-enrollment-status-report"></a><span data-ttu-id="98282-127">Sestava stavu registrace k zaměstnaneckým výhodám</span><span class="sxs-lookup"><span data-stu-id="98282-127">Benefit enrollment status report</span></span>

<span data-ttu-id="98282-128">Vestavěné výkaznictví u otevřené registrace k zaměstnaneckým výhodám snadno pochopit, kde se nachází zaměstnanci v procesu otevřené registrace.</span><span class="sxs-lookup"><span data-stu-id="98282-128">Built-in reporting about open enrollment for benefits helps you easily understand where your employees are in the open enrollment process.</span></span> <span data-ttu-id="98282-129">Můžete zjistit, kolik zaměstnanců dokončilo proces, kolik ho aktuálně dokončuje a kolik jich ještě nezačalo.</span><span class="sxs-lookup"><span data-stu-id="98282-129">You can learn how many employees have completed the process, are currently completing it, and haven't started it.</span></span> <span data-ttu-id="98282-130">Navíc můžete rychle zobrazit problémy, ke kterým došlo při registraci zaměstnance, a celý protokol všech odeslání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="98282-130">Additionally, you can quickly view any issues that occur during employee enrollment and a full log of all employee submissions.</span></span> <span data-ttu-id="98282-131">Lze tedy snadno ověřit a auditovat odeslání zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="98282-131">Therefore, you can easily verify and audit employee submissions.</span></span>
