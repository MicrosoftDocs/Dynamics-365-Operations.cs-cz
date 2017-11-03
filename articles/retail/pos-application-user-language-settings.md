---
title: "Uživatelské nastavení a nastavení jazyka aplikace POS"
description: "Toto téma popisuje, jak změnit nastavení jazyka v Retail Modern POS (MPOS) a Cloud POS."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dacc072ab5c070010d86302fa08a3066125b23a6
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="05ba1-103">Uživatelské nastavení a nastavení jazyka aplikace POS</span><span class="sxs-lookup"><span data-stu-id="05ba1-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="05ba1-104">Toto téma popisuje, jak změnit nastavení jazyka v Retail Modern POS (MPOS) a Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="05ba1-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="05ba1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="05ba1-105">Overview</span></span>
========

<span data-ttu-id="05ba1-106">Retail Modern POS (MPOS) a Cloud POS podporují prostředí, kde se může nastavení jazyka a překlady lišit mezi nastavením obchodu a uživatelským nastavením.</span><span class="sxs-lookup"><span data-stu-id="05ba1-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="05ba1-107">Obchod se může například nacházet v oblasti, kde zákazníci preferují angličtinu, ale někteří pracovníci dávají přednost používání aplikací s francouzskými překlady.</span><span class="sxs-lookup"><span data-stu-id="05ba1-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="05ba1-108">Jazyk dat</span><span class="sxs-lookup"><span data-stu-id="05ba1-108">Data language</span></span>
<span data-ttu-id="05ba1-109">Bez ohledu na uživatelské nastavení bude MPOS a Cloud POS vždy používat nastavení jazyka obchodu k určení překladů používaných pro data.</span><span class="sxs-lookup"><span data-stu-id="05ba1-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="05ba1-110">Tím se zajistí, že všichni uživatelé a zákazníci budou mít konzistentní zkušenosti.</span><span class="sxs-lookup"><span data-stu-id="05ba1-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="05ba1-111">Příklady popisů dat:</span><span class="sxs-lookup"><span data-stu-id="05ba1-111">Examples of data include:</span></span>

-   <span data-ttu-id="05ba1-112">Produkty</span><span class="sxs-lookup"><span data-stu-id="05ba1-112">Products</span></span>
-   <span data-ttu-id="05ba1-113">Atributy a hodnoty</span><span class="sxs-lookup"><span data-stu-id="05ba1-113">Attributes and values</span></span>
-   <span data-ttu-id="05ba1-114">Názvy kategorie</span><span class="sxs-lookup"><span data-stu-id="05ba1-114">Category names</span></span>
-   <span data-ttu-id="05ba1-115">Tištěné nebo e-mailem odeslané transakční příjmy</span><span class="sxs-lookup"><span data-stu-id="05ba1-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="05ba1-116">Názvy způsobu platby</span><span class="sxs-lookup"><span data-stu-id="05ba1-116">Payment method names</span></span>
-   <span data-ttu-id="05ba1-117">Zprávy řádkového displeje</span><span class="sxs-lookup"><span data-stu-id="05ba1-117">Line display messages</span></span>

<span data-ttu-id="05ba1-118">Jazyk obchodu bude použit také pro hlavní přihlašovací obrazovku POS, protože uživatel není znám před přihlášením.</span><span class="sxs-lookup"><span data-stu-id="05ba1-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="05ba1-119">Pokud překlad není k dispozici pro jazyk obchodu, POS se vrátí k jazyku společnosti.</span><span class="sxs-lookup"><span data-stu-id="05ba1-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="05ba1-120">Konfigurace nastavení jazyka obchodu</span><span class="sxs-lookup"><span data-stu-id="05ba1-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="05ba1-121">Jazyko obchodu se nastavuje ve složce **Všechny maloobchody** na stránce **Maloobchod** v části **Obecné &gt; Regionální nastavení &gt; Jazyk.</span><span class="sxs-lookup"><span data-stu-id="05ba1-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="05ba1-122">**Pomocí rozevíracího seznamu vyberte jazyk pro každý obchod.</span><span class="sxs-lookup"><span data-stu-id="05ba1-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="05ba1-123">Jazyk uživatelského rozhraní</span><span class="sxs-lookup"><span data-stu-id="05ba1-123">User interface language</span></span>
<span data-ttu-id="05ba1-124">Nastavení jazyka uživatele POS určuje překlady používané v uživatelském rozhraní aplikace.</span><span class="sxs-lookup"><span data-stu-id="05ba1-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="05ba1-125">Jedná se o všechny popisky, nabídky a seznamy, které nejsou považovány za data.</span><span class="sxs-lookup"><span data-stu-id="05ba1-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="05ba1-126">Jedinou výjimkou je text, který je zobrazen na tlačítkách mřížky POS.</span><span class="sxs-lookup"><span data-stu-id="05ba1-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="05ba1-127">Tlačítka mřížky nepodporují překlady, takže budou vždy zobrazovaly text definovaný na tlačítku.</span><span class="sxs-lookup"><span data-stu-id="05ba1-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="05ba1-128">Abyste získali podporu přeložených tlačítek, budete muset zkopírovat a udržovat samostatné mřížky tlačítek a přiřadit je uživatelům podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="05ba1-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="05ba1-129">Konfigurace nastavení jazyka uživatele</span><span class="sxs-lookup"><span data-stu-id="05ba1-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="05ba1-130">Jazyk uživatele POS se nastavuje v okně **Všichni pracovníci** na stránce **Pracovník** pod **Maloobchod &gt; Jazyk**.</span><span class="sxs-lookup"><span data-stu-id="05ba1-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="05ba1-131">Není nastaveno na hlavní kartě Profil.  Toto nastavení není použito v programu POS.</span><span class="sxs-lookup"><span data-stu-id="05ba1-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="05ba1-132">Pokud není jazyk uživatele nastaven, nebo pokud je nastaven na jazyk, pro který nejsou k dispozici překlady, POS obnoví používání jazyka obchodu.</span><span class="sxs-lookup"><span data-stu-id="05ba1-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="05ba1-133">** **</span><span class="sxs-lookup"><span data-stu-id="05ba1-133">** **</span></span>       | <span data-ttu-id="05ba1-134">**Jazyk uživatelského rozhraní** ** **</span><span class="sxs-lookup"><span data-stu-id="05ba1-134">**UI language** ** **</span></span>      | <span data-ttu-id="05ba1-135">**Jazyk dat (produkty, formáty příjemky, řádkový displej atd.)**</span><span class="sxs-lookup"><span data-stu-id="05ba1-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="05ba1-136">**Company (Společnost)**</span><span class="sxs-lookup"><span data-stu-id="05ba1-136">**Company**</span></span> | <span data-ttu-id="05ba1-137">Výchozí</span><span class="sxs-lookup"><span data-stu-id="05ba1-137">Default</span></span>                    | <span data-ttu-id="05ba1-138">Výchozí</span><span class="sxs-lookup"><span data-stu-id="05ba1-138">Default</span></span>                                                           |
| <span data-ttu-id="05ba1-139">**Obchod**</span><span class="sxs-lookup"><span data-stu-id="05ba1-139">**Store**</span></span>   | <span data-ttu-id="05ba1-140">Přepsání společnosti</span><span class="sxs-lookup"><span data-stu-id="05ba1-140">Overrides company</span></span>          | <span data-ttu-id="05ba1-141">Přepsání společnosti</span><span class="sxs-lookup"><span data-stu-id="05ba1-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="05ba1-142">**Uživatel**</span><span class="sxs-lookup"><span data-stu-id="05ba1-142">**User**</span></span>    | <span data-ttu-id="05ba1-143">Přepsání obchodu nebo společnosti</span><span class="sxs-lookup"><span data-stu-id="05ba1-143">Overrides store or company</span></span> | <span data-ttu-id="05ba1-144">Nikdy</span><span class="sxs-lookup"><span data-stu-id="05ba1-144">Never</span></span>                                                             |






