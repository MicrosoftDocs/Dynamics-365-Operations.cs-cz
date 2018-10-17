---
title: "Kusovníky šablony"
description: "Kusovník šablony poskytuje standardní seznam součástí pro předměty servisu, o které pravidelně pečujete."
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/21/2018

---

# <a name="template-boms"></a><span data-ttu-id="7374d-103">Kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="7374d-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7374d-104">Kusovník šablony poskytuje standardní seznam součástí pro předměty servisu, o které pravidelně pečujete.</span><span class="sxs-lookup"><span data-stu-id="7374d-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="7374d-105">Součásti uvedené v kusovníku šablony představují jednotlivé dílčí součásti předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="7374d-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="7374d-106">Když na předmět servisu použijete kusovník šablony, můžete uchovávat záznam dílčích součástí, které byly v předmětu servisu vyměněny.</span><span class="sxs-lookup"><span data-stu-id="7374d-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="7374d-107">Použití kusovníku šablony na servisní smlouvu nebo zakázku vyžaduje jeho připojení ke vztahu předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="7374d-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7374d-108">Na předmět servisu lze použít pouze jeden kusovník šablony.</span><span class="sxs-lookup"><span data-stu-id="7374d-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="7374d-109">Vytvoření šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="7374d-109">Create a template BOM</span></span>

<span data-ttu-id="7374d-110">Následující tabulka obsahuje informace o různých metodách používaných k vytvoření šablony Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7374d-111">Metoda</span><span class="sxs-lookup"><span data-stu-id="7374d-111">Method</span></span></p></th>
<th><p><span data-ttu-id="7374d-112">popis</span><span class="sxs-lookup"><span data-stu-id="7374d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7374d-113">Výrobní</span><span class="sxs-lookup"><span data-stu-id="7374d-113">Production</span></span></p></td>
<td><p><span data-ttu-id="7374d-114">Šablona kusovníku je založena na výrobní zakázce.</span><span class="sxs-lookup"><span data-stu-id="7374d-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="7374d-115">Tato možnost je k dispozici pouze v případě, že pracujete v produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="7374d-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="7374d-116">Výhodou je, že máte aktuální, podrobný seznam součástí, které tvoří položku.</span><span class="sxs-lookup"><span data-stu-id="7374d-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7374d-117">Položka BOM</span><span class="sxs-lookup"><span data-stu-id="7374d-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="7374d-118">Šablona kusovníku je vytvořena na základě kusovníku položky.</span><span class="sxs-lookup"><span data-stu-id="7374d-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="7374d-119">Kusovník položky, na rozdíl od výrobního Kusovníku, je statický seznam součástí, ze kterých je položka sestavena.</span><span class="sxs-lookup"><span data-stu-id="7374d-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7374d-120">Stávající šablona</span><span class="sxs-lookup"><span data-stu-id="7374d-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="7374d-121">Tato šablona je vytvořena na základě existujícího kusovníku položky.</span><span class="sxs-lookup"><span data-stu-id="7374d-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7374d-122">Ruční</span><span class="sxs-lookup"><span data-stu-id="7374d-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="7374d-123">Pokud víte, které náhradní díly obvykle měníte v předmětu servisu, můžete ručně vytvořit šablonu kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="7374d-124">Tato metoda napomáhá k zajištění, že součásti, které jsou zahrnuty do šablony, odpovídají skutečným požadavkům vašeho pracoviště.</span><span class="sxs-lookup"><span data-stu-id="7374d-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="7374d-125">Použití kusovníku šablony na servisní smlouvu nebo zakázku</span><span class="sxs-lookup"><span data-stu-id="7374d-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="7374d-126">Kusovník šablony můžete použít na servisní smlouvu nebo servisní zakázku nebo na obojí.</span><span class="sxs-lookup"><span data-stu-id="7374d-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="7374d-127">Servisní smlouva obvykle pokrývá dlouhodobou spolupráci s odběratelem.</span><span class="sxs-lookup"><span data-stu-id="7374d-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="7374d-128">Užitečnými informacemi, které je třeba zaznamenat v servisní smlouvě, je historie výměn, která jsou sledovány v servisním kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="7374d-129">Šablonu Kusovníku lze také použít na servisní zakázku a zaznamenávat historii služby, která byla provedena v předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="7374d-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="7374d-130">Zkopírování historie servisního kusovníku</span><span class="sxs-lookup"><span data-stu-id="7374d-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="7374d-131">Historii řádků servisního kusovníku lze zkopírovat z jedné servisní smlouvy do jiné smlouvy.</span><span class="sxs-lookup"><span data-stu-id="7374d-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="7374d-132">Zkopírováním historie servisu mezi smlouvami můžete zachovat záznam o výměnách položky.</span><span class="sxs-lookup"><span data-stu-id="7374d-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="7374d-133">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="7374d-133">**Example**</span></span>

<span data-ttu-id="7374d-134">Uzavřeli jste tříletou servisní smlouvu na auto odběratele.</span><span class="sxs-lookup"><span data-stu-id="7374d-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="7374d-135">Během tohoto období si odběratel zvykne na vysokou úroveň služeb, kterou společnost poskytuje.</span><span class="sxs-lookup"><span data-stu-id="7374d-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="7374d-136">Proto po vypršení smlouvy chce tento zákazník zadat novou.</span><span class="sxs-lookup"><span data-stu-id="7374d-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="7374d-137">Máte nyní možnost dohodnout výhodnější smluvní podmínky pro společnost.</span><span class="sxs-lookup"><span data-stu-id="7374d-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="7374d-138">Vzhledem k tomu, že záznamy o vyměněných součástech mohou být v budoucnosti užitečné, zkopírujete historii servisního kusovníku do nové smlouvy.</span><span class="sxs-lookup"><span data-stu-id="7374d-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="7374d-139">Úprava kusovníku šablony</span><span class="sxs-lookup"><span data-stu-id="7374d-139">Modify the template BOM</span></span>

<span data-ttu-id="7374d-140">Pokud šablona Kusovníku nebyla připojena k předmětu servisu, můžete z ní upravit nebo odstranit řádky.</span><span class="sxs-lookup"><span data-stu-id="7374d-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="7374d-141">Po připojení šablony Kusovníku k určitému předmětu servisu můžete upravit místní verzi Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="7374d-142">Pokud chcete duplikovat nastavení místní verze Kusovníku šablony, můžete vytvořit novou šablonu Kusovníku na základě místní verze.</span><span class="sxs-lookup"><span data-stu-id="7374d-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="7374d-143">Další informace získáte v tématu [Změna kusovníku služby](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="7374d-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="7374d-144">Pokud nahradíte položku v kusovníku, můžete výměnu zaznamenat v řádku kusovníku, který je k dispozici v návrháři kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="7374d-145">Volitelně můžete pro vyměněný objekt vystavit fakturu.</span><span class="sxs-lookup"><span data-stu-id="7374d-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="7374d-146">Jestliže vytvoříte řádek servisní zakázky, můžete pro vyměněnou součást vystavit fakturu.</span><span class="sxs-lookup"><span data-stu-id="7374d-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="7374d-147">Pokud pro výměnu nevytvoříte řádek servisní zakázky, uchovají se pro vaše záznamy informace o výměně a sleduje se historie předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="7374d-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="7374d-148">Změna způsobu zobrazení informací na řádku Kusovníku</span><span class="sxs-lookup"><span data-stu-id="7374d-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="7374d-149">Pro všechny kusovníky šablon a servisní kusovníky můžete určit, jakým způsobem se mají zobrazovat informace z řádků kusovníků.</span><span class="sxs-lookup"><span data-stu-id="7374d-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="7374d-150">Tyto změny se vztahují na všechny kusovníky šablony a kusovníky servisu.</span><span class="sxs-lookup"><span data-stu-id="7374d-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="7374d-151">Patří sem ty, které jsou připojeny k předmětům servisu.</span><span class="sxs-lookup"><span data-stu-id="7374d-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="7374d-152">Nastavení číselných řad pro kusovníky šablony</span><span class="sxs-lookup"><span data-stu-id="7374d-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="7374d-153">Chcete-li používat kusovníky šablony, je nutné nastavit dvě číselné řady.</span><span class="sxs-lookup"><span data-stu-id="7374d-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="7374d-154">Jedna řada je určená pro kusovník šablony a druhá pro číslování řádků historie kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7374d-155">Číselné řady se používají k přidělování identifikátorů k záznamům, které je vyžadují.</span><span class="sxs-lookup"><span data-stu-id="7374d-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="7374d-156">Aby bylo možné přiřadit číselnou řadu pro Kusovník šablony nebo číslo řádku historie Kusovníku, musíte nastavit kódy číselných řad.</span><span class="sxs-lookup"><span data-stu-id="7374d-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="7374d-157">Nastavit číselné řady</span><span class="sxs-lookup"><span data-stu-id="7374d-157">Set up number sequences</span></span>

1.  <span data-ttu-id="7374d-158">Na stránce se seznamem **číselné řady** vytvořte číselné řady pro kusovníky šablony a čísla řádků historie Kusovníku.</span><span class="sxs-lookup"><span data-stu-id="7374d-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="7374d-159">Klikněte **Správa servisu** \> **Nastavení** \> **Parametry správy servisu**.</span><span class="sxs-lookup"><span data-stu-id="7374d-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="7374d-160">Klepněte na tlačítko **číselné řady**a vyberte kód číselné řady pro reference číselné řady, které jste vytvořili ve formuláři **číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="7374d-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="7374d-161">Uložte změny zavřením formuláře.</span><span class="sxs-lookup"><span data-stu-id="7374d-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7374d-162">Číslo řádku historie Kusovníku používá systém k přidružení transakcí v historii Kusovníku k servisní smlouvě nebo servisní zakázce.</span><span class="sxs-lookup"><span data-stu-id="7374d-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="7374d-163">Číslo řádku historie kusovníku se nezobrazuje v uživatelském rozhraní.</span><span class="sxs-lookup"><span data-stu-id="7374d-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="7374d-164">Viz také</span><span class="sxs-lookup"><span data-stu-id="7374d-164">See also</span></span>

[<span data-ttu-id="7374d-165">Vytvoření šablony kusovníku</span><span class="sxs-lookup"><span data-stu-id="7374d-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="7374d-166">Správa šablon kusovníku pro vztahy předmětu</span><span class="sxs-lookup"><span data-stu-id="7374d-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="7374d-167">Změna servisního kusovníku</span><span class="sxs-lookup"><span data-stu-id="7374d-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



