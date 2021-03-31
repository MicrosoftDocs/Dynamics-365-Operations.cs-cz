---
title: Kódy kroku vlny
description: V tomto tématu je uveden přehled kódů kroků vlny a jejich použití.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c28134b9be92802196b4861cbd20801419ef8d23
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212668"
---
# <a name="wave-step-codes"></a><span data-ttu-id="b3516-103">Kódy kroku vlny</span><span class="sxs-lookup"><span data-stu-id="b3516-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3516-104">Kódy kroků vlny jsou kódy, které mohou uživatelé nastavit a použít k propojení určitých instancí metod vlny s odpovídající šablonou.</span><span class="sxs-lookup"><span data-stu-id="b3516-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="b3516-105">Tyto šablony zahrnují šablony pro doplnění, vytváření kontejnerů, tisk štítků, sestavení a třídění.</span><span class="sxs-lookup"><span data-stu-id="b3516-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="b3516-106">Nejsou-li kódy kroků vlny použity, uživatelé musí zadat volný text, který bude odkazovat na určitou šablonu z instance metody vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="b3516-107">Volný text je náchylný k chybám, protože uživatelé se musí ujistit, že text kroku vlny, který přidávají pro specifickou metodu vlny v šabloně vlny, přesně odpovídá textu kroku vlny v cílové šabloně.</span><span class="sxs-lookup"><span data-stu-id="b3516-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="b3516-108">Kódy kroků vlny pro určitý typ kroku vlny jsou nastaveny na samostatné stránce.</span><span class="sxs-lookup"><span data-stu-id="b3516-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="b3516-109">Pro každou instanci metody kroku vlny v šabloně vlny, která vyžaduje kód kroku vlny, musí být v rozevíracím seznamu vybrán kód kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="b3516-110">Výběr v rozevíracím seznamu nahrazuje zadávání volného textu a pomáhá snižovat riziko a dopad lidských chyb.</span><span class="sxs-lookup"><span data-stu-id="b3516-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="b3516-111">Kódy nastavení se používají k propojení metody kroku vlny v šabloně vlny s cílovou šablonou pro metodu.</span><span class="sxs-lookup"><span data-stu-id="b3516-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="b3516-112">Použití funkce kódů kroku vlny je nepovinné.</span><span class="sxs-lookup"><span data-stu-id="b3516-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="b3516-113">Je povolena celá organizace pro všechny právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="b3516-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="b3516-114">Nastavení ukázky</span><span class="sxs-lookup"><span data-stu-id="b3516-114">Setup demo</span></span> 

<span data-ttu-id="b3516-115">Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b3516-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="b3516-116">Povolit kódy kroku vlny</span><span class="sxs-lookup"><span data-stu-id="b3516-116">Enable wave step codes</span></span>

<span data-ttu-id="b3516-117">Pomocí následujících kroků zapněte funkci kódů kroků vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="b3516-118">Přejděte na **Správu funkcí**.</span><span class="sxs-lookup"><span data-stu-id="b3516-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="b3516-119">Výběrem této možnosti povolíte funkci nazvanou **Kód kroku vlny pro celou organizaci**.</span><span class="sxs-lookup"><span data-stu-id="b3516-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="b3516-120">Všechny existující volné texty ve všech právnických osobách jsou upgradovány na novou strukturu.</span><span class="sxs-lookup"><span data-stu-id="b3516-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="b3516-121">Po dokončení upgradu pro všechny právnické osoby je tato funkce povolena.</span><span class="sxs-lookup"><span data-stu-id="b3516-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="b3516-122">Pokud funkci nelze povolit pro jednu nebo více právnických osob, nebude tato funkce povolena pro žádné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="b3516-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="b3516-123">Během upgradu jsou během inovace dat provedeny ověření.</span><span class="sxs-lookup"><span data-stu-id="b3516-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="b3516-124">Pokud se inovace nezdaří, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="b3516-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="b3516-125">Upgrade se nemusí zdařit kvůli následujícím konfliktům:</span><span class="sxs-lookup"><span data-stu-id="b3516-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="b3516-126">Existují duplicitní texty volného kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="b3516-127">Existují přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="b3516-127">Customizations exist.</span></span>
- <span data-ttu-id="b3516-128">Volný text v kroku vlny, který je přidružen k instanci metody kroku vlny, neodpovídá očekávanému typu šablony.</span><span class="sxs-lookup"><span data-stu-id="b3516-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="b3516-129">Po vyřešení konfliktů, které byly zjištěny během ověření, můžete znovu zkusit povolit funkci.</span><span class="sxs-lookup"><span data-stu-id="b3516-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="b3516-130">Po povolení funkce bude k dispozici stránka **kódy kroků vlny** (**Řízení skladu \> Nastavení \> Vlny \> Kódy nastavení vlny**).</span><span class="sxs-lookup"><span data-stu-id="b3516-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="b3516-131">Na této stránce jsou uvedeny kódy kroků vlny, které byly upgradovány při zapnutí funkce kódy kroků vlny pro celou organizaci.</span><span class="sxs-lookup"><span data-stu-id="b3516-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="b3516-132">Vytvořit nové kódy kroků vlny</span><span class="sxs-lookup"><span data-stu-id="b3516-132">Create new wave step codes</span></span>

<span data-ttu-id="b3516-133">Stránku **kódy kroků vlny** můžete použít k vytváření a odstraňování kódů kroků vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="b3516-134">Každý nový kód kroku vlny a jeho přidružené ID musí být jedinečné napříč všemi typy kroků vlny a musí být definovány pro určitý typ kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="b3516-135">Použití kódů kroků vlny</span><span class="sxs-lookup"><span data-stu-id="b3516-135">Apply wave step codes</span></span>

<span data-ttu-id="b3516-136">Po definování příslušných kódů kroků vlny je lze použít na metody procesu vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="b3516-137">Chcete-li použít kódy kroků vlny, přejděte na příslušnou cílovou šablonu.</span><span class="sxs-lookup"><span data-stu-id="b3516-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="b3516-138">Zde jsou cílové šablony, pro které jsou označeny kódy kroků vlny na:</span><span class="sxs-lookup"><span data-stu-id="b3516-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="b3516-139">**Šablony doplnění:** Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění</span><span class="sxs-lookup"><span data-stu-id="b3516-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="b3516-140">**Načíst šablony sestavení:** Řízení skladu \> Nastavení \> Načíst \> Načíst šablony sestavení</span><span class="sxs-lookup"><span data-stu-id="b3516-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="b3516-141">**Seřadit šablony:** Řízení skladu \> Nastavení \> Balení \> Odchozí šablony řazení</span><span class="sxs-lookup"><span data-stu-id="b3516-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="b3516-142">**Šablony vytváření kontejnerů:** Řízení skladu \> Nastavení \> Kontejnery \> Šablony sestavení kontejneru</span><span class="sxs-lookup"><span data-stu-id="b3516-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="b3516-143">**Štítky pro tisk štítků**: Řízení skladu \> Nastavení \> Směrování dokumentu \> Šablony štítku vlny</span><span class="sxs-lookup"><span data-stu-id="b3516-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="b3516-144">Šablony v tomto seznamu jsou použity, pokud jsou odkazovány z metody procesu vlny vybrané v šabloně vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="b3516-145">Když kód kroku vlny u metody procesu vlny v šabloně vlny odpovídá kódu kroku vlny v jednom z typů šablon, použije se šablona.</span><span class="sxs-lookup"><span data-stu-id="b3516-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="b3516-146">Ukázkový scénář</span><span class="sxs-lookup"><span data-stu-id="b3516-146">Sample scenario</span></span>

<span data-ttu-id="b3516-147">Následující postup vám pomůže zaručit, že vytvořená šablona doplnění bude použita pro šablonu vlny.</span><span class="sxs-lookup"><span data-stu-id="b3516-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="b3516-148">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny** a vytvořte kód kroku vlny pro typ **doplnění**.</span><span class="sxs-lookup"><span data-stu-id="b3516-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="b3516-149">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění** a vytvořte šablonu doplnění.</span><span class="sxs-lookup"><span data-stu-id="b3516-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="b3516-150">V šabloně doplnění vyberte kód kroku vlny, který jste vytvořili pro typ **doplnění**.</span><span class="sxs-lookup"><span data-stu-id="b3516-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="b3516-151">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny** a vyberte šablonu vlny, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="b3516-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="b3516-152">V šabloně na pevné záložce **Metody** vyberte metodu **Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="b3516-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="b3516-153">V poli **Kód kroku vlny** vyberte kód kroku vlny, který jste vybrali v šabloně doplnění.</span><span class="sxs-lookup"><span data-stu-id="b3516-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="b3516-154">Tyto kroky provedete pro každou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="b3516-154">You perform these steps for each legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]