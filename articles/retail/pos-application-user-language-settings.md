---
title: "Nastavení pokladního místa (POS) a uživatelského jazyka"
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
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: faf8cdcee70b55842072298b51789f6cd7a577af
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="7fdf5-103">Nastavení pokladního místa (POS) a uživatelského jazyka</span><span class="sxs-lookup"><span data-stu-id="7fdf5-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7fdf5-104">Toto téma popisuje, jak změnit nastavení jazyka v Retail Modern POS (MPOS) a Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="7fdf5-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="7fdf5-105">Overview</span></span>

<span data-ttu-id="7fdf5-106">Retail Modern POS (MPOS) a Cloud POS podporují prostředí, kde se může nastavení jazyka a překlady lišit mezi nastavením obchodu a uživatelským nastavením.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="7fdf5-107">Obchod se může například nacházet v oblasti, kde zákazníci preferují angličtinu, ale někteří pracovníci dávají přednost používání aplikací s francouzskými překlady.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="7fdf5-108">Jazyk dat</span><span class="sxs-lookup"><span data-stu-id="7fdf5-108">Data language</span></span>

<span data-ttu-id="7fdf5-109">Bez ohledu na uživatelské nastavení bude MPOS a Cloud POS vždy používat nastavení jazyka obchodu k určení překladů používaných pro data.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="7fdf5-110">Tím se zajistí, že všichni uživatelé a zákazníci budou mít konzistentní zkušenosti.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="7fdf5-111">Příklady popisů dat:</span><span class="sxs-lookup"><span data-stu-id="7fdf5-111">Examples of data include:</span></span>

- <span data-ttu-id="7fdf5-112">Produkty</span><span class="sxs-lookup"><span data-stu-id="7fdf5-112">Products</span></span>
- <span data-ttu-id="7fdf5-113">Atributy a hodnoty</span><span class="sxs-lookup"><span data-stu-id="7fdf5-113">Attributes and values</span></span>
- <span data-ttu-id="7fdf5-114">Názvy kategorie</span><span class="sxs-lookup"><span data-stu-id="7fdf5-114">Category names</span></span>
- <span data-ttu-id="7fdf5-115">Tištěné nebo e-mailem odeslané transakční příjmy</span><span class="sxs-lookup"><span data-stu-id="7fdf5-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="7fdf5-116">Názvy způsobu platby</span><span class="sxs-lookup"><span data-stu-id="7fdf5-116">Payment method names</span></span>
- <span data-ttu-id="7fdf5-117">Zprávy řádkového displeje</span><span class="sxs-lookup"><span data-stu-id="7fdf5-117">Line display messages</span></span>

<span data-ttu-id="7fdf5-118">Jazyk obchodu bude použit také pro hlavní přihlašovací obrazovku POS, protože uživatel není znám před přihlášením.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="7fdf5-119">Pokud překlad není k dispozici pro jazyk obchodu, POS se vrátí k jazyku společnosti.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="7fdf5-120">Konfigurace nastavení jazyka obchodu</span><span class="sxs-lookup"><span data-stu-id="7fdf5-120">Configuring the store's language setting</span></span>

<span data-ttu-id="7fdf5-121">Jazyko obchodu se nastavuje ve složce **Všechny maloobchody** na stránce **Maloobchod** v části **Obecné &gt; Regionální nastavení &gt; Jazyk**.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-121">The store's language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="7fdf5-122">Pomocí rozevíracího seznamu vyberte jazyk pro každý obchod.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-122">Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="7fdf5-123">Jazyk uživatelského rozhraní</span><span class="sxs-lookup"><span data-stu-id="7fdf5-123">User interface language</span></span>

<span data-ttu-id="7fdf5-124">Nastavení jazyka uživatele POS určuje překlady používané v uživatelském rozhraní aplikace.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="7fdf5-125">Jedná se o všechny popisky, nabídky a seznamy, které nejsou považovány za data.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="7fdf5-126">Jedinou výjimkou je text, který je zobrazen na tlačítkách mřížky POS.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="7fdf5-127">Tlačítka mřížky nepodporují překlady, takže budou vždy zobrazovaly text definovaný na tlačítku.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="7fdf5-128">Abyste získali podporu přeložených tlačítek, budete muset zkopírovat a udržovat samostatné mřížky tlačítek a přiřadit je uživatelům podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="7fdf5-129">Konfigurace nastavení jazyka uživatele</span><span class="sxs-lookup"><span data-stu-id="7fdf5-129">Configuring the user's language setting</span></span>

<span data-ttu-id="7fdf5-130">Nastavení jazyka uživatele POS pochází z nabídky **Všichni pracovníci** na stránce **Pracovník** v části **Maloobchod &gt; Jazyk**.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span> <span data-ttu-id="7fdf5-131">Není nastaveno na hlavní kartě Profil. Toto nastavení není použito v programu POS.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="7fdf5-132">Pokud není jazyk uživatele nastaven, nebo pokud je nastaven na jazyk, pro který nejsou k dispozici překlady, POS obnoví používání jazyka obchodu.</span><span class="sxs-lookup"><span data-stu-id="7fdf5-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="7fdf5-133">Jazyk UR  </span><span class="sxs-lookup"><span data-stu-id="7fdf5-133">UI language</span></span>                | <span data-ttu-id="7fdf5-134">Jazyk dat (produkty, formáty příjemky, řádkový displej atd.)</span><span class="sxs-lookup"><span data-stu-id="7fdf5-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7fdf5-135">**Company (Společnost)**</span><span class="sxs-lookup"><span data-stu-id="7fdf5-135">**Company**</span></span> | <span data-ttu-id="7fdf5-136">Výchozí</span><span class="sxs-lookup"><span data-stu-id="7fdf5-136">Default</span></span>                    | <span data-ttu-id="7fdf5-137">Výchozí</span><span class="sxs-lookup"><span data-stu-id="7fdf5-137">Default</span></span>                                                       |
| <span data-ttu-id="7fdf5-138">**Obchod**</span><span class="sxs-lookup"><span data-stu-id="7fdf5-138">**Store**</span></span>   | <span data-ttu-id="7fdf5-139">Přepsání společnosti</span><span class="sxs-lookup"><span data-stu-id="7fdf5-139">Overrides company</span></span>          | <span data-ttu-id="7fdf5-140">Přepsání společnosti</span><span class="sxs-lookup"><span data-stu-id="7fdf5-140">Overrides company</span></span>                                             |
| <span data-ttu-id="7fdf5-141">**Uživatel**</span><span class="sxs-lookup"><span data-stu-id="7fdf5-141">**User**</span></span>    | <span data-ttu-id="7fdf5-142">Přepsání obchodu nebo společnosti</span><span class="sxs-lookup"><span data-stu-id="7fdf5-142">Overrides store or company</span></span> | <span data-ttu-id="7fdf5-143">Nikdy</span><span class="sxs-lookup"><span data-stu-id="7fdf5-143">Never</span></span>                                                         |

