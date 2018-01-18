---
title: "Rozšíření funkce Microsoft Dynamics 365 for Talent"
description: "Pokud jste vytvořili jakoukoliv aplikaci Microsoft PowerApps, můžete spustit tyto aplikace z odkazů v rámci aplikace Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Talent
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 80f6d4e54d103b4511cbbbcce75ee29e8a04811b
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="f4e8b-103">Rozšíření funkce Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="f4e8b-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>
<span data-ttu-id="f4e8b-104">Pokud jste vytvořili jakoukoliv aplikaci Microsoft PowerApps, můžete spustit tyto aplikace z odkazů v rámci aplikace Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="f4e8b-105">Chcete-li nastavit přístup ke svým aplikacím, musíte nastavit některé informace v aplikaci Talent na stránce konfigurace, kterou lze otevřít z pracovního prostoru **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="f4e8b-106">Konfigurace integrovaných aplikací PowerApps v rámci aplikace Talent</span><span class="sxs-lookup"><span data-stu-id="f4e8b-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="f4e8b-107">Použijte stránku **Nastavení integrovaných aplikací Microsoft PowerApps** pro konfiguraci stránek Talent slouží ke spuštění aplikací PowerApps.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="f4e8b-108">Chcete-li otevřít stránku **Nastavení integrovaných aplikací Microsoft PowerApps**, otevřete pracovní prostor **Správa systému** a potom otevřete kartu **Odkazy**. Zvolte **Microsoft PowerApps** ze skupiny **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="f4e8b-109">Na této stránce se zadávají nebo nastavují následující informace:</span><span class="sxs-lookup"><span data-stu-id="f4e8b-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="f4e8b-110">Popisný název nebo identifikátor pro každou aplikaci PowerApps.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="f4e8b-111">Jedinečný identifikátor (GUID) pro každou aplikaci přidanou na stránku Talent.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="f4e8b-112">ID aplikace je k dispozici na webu PowerApps [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="f4e8b-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="f4e8b-113">Stránka, odkud mohou uživatelé otevřít aplikaci nebo sestavu.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="f4e8b-114">Ne všechny stránky Talent podporují integrované aplikace PowerApps a sestavy Power BI.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="f4e8b-115">Zadejte interní název stránky, nikoli zobrazovaný název, který je zobrazen v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="f4e8b-116">K vyhledání interního názvu otevřete stránku, jejíž interní název potřebujete, a kamkoli klikněte pravým tlačítkem na stránce.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="f4e8b-117">Po otevření nabídky najeďte myší nad položku **Informace formuláře**.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="f4e8b-118">Interní název formuláře se zobrazí vedle položky menu **Informace formuláře**.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="f4e8b-119">Určete ovládací prvek formuláře, ze kterého aplikace může načíst kontextová data.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="f4e8b-120">Aplikace může například použít data týkající se pracovníka.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="f4e8b-121">Pokud zadáte stránku **Pracovník** do pole **Kontext**, otevře se stránka **Pracovník** při spuštění aplikace.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="f4e8b-122">Zadání do **kontextového pole** není povinné.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="f4e8b-123">Nastavte velikost dialogové okno, ve kterém bude spuštěna aplikace PowerApps.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="f4e8b-124">Dialogová okna jsou označena jako malá nebo velká pro optimalizaci uživatelského rozhraní pro spuštění vaší aplikace buď na telefonu nebo na větším zařízení.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="f4e8b-125">Můžete také určit, pro které právnické osoby bude aplikace dostupná, nebo ji můžete zpřístupnit pro všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="f4e8b-126">Standardně jsou aplikace PowerApps k dispozici pro všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="f4e8b-127">Otevření aplikace</span><span class="sxs-lookup"><span data-stu-id="f4e8b-127">Opening an application</span></span>
<span data-ttu-id="f4e8b-128">Po dokončení konfigurace integrované aplikace PowerApps se přidají odkazy na vámi určené aplikace na stránky v rámci aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="f4e8b-129">Klikněte na odkaz, pokud chcete aplikaci otevřít.</span><span class="sxs-lookup"><span data-stu-id="f4e8b-129">Click a link to open an application.</span></span> 



