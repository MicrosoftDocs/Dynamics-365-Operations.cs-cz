---
title: Řešení potíží s informacemi o produktu
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s informacemi o produktu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9db8e0081a0d47ec8d74680fe99a0934b99bb5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223355"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="cceca-103">Řešení potíží s informacemi o produktu</span><span class="sxs-lookup"><span data-stu-id="cceca-103">Troubleshoot product information</span></span>

<span data-ttu-id="cceca-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s informacemi o produktu.</span><span class="sxs-lookup"><span data-stu-id="cceca-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="cceca-105">Nemohu odstranit uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="cceca-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-106">Issue description</span></span>

<span data-ttu-id="cceca-107">Uvolněný produkt a všechny jeho varianty můžete odstranit, pouze pokud uvolněný produkt nemá žádné související transakce.</span><span class="sxs-lookup"><span data-stu-id="cceca-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-108">Issue resolution</span></span>

<span data-ttu-id="cceca-109">Podle těchto pokynů odstraníte uvolněný produkt nebo základní produkt.</span><span class="sxs-lookup"><span data-stu-id="cceca-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="cceca-110">Zavřete všechny otevřené transakce pro položky.</span><span class="sxs-lookup"><span data-stu-id="cceca-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="cceca-111">Snižte zásoby na 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="cceca-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="cceca-112">Proveďte uzávěrku skladu.</span><span class="sxs-lookup"><span data-stu-id="cceca-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="cceca-113">Odstraňte všechny varianty produktu pro hlavní produkt, který chcete odstranit.</span><span class="sxs-lookup"><span data-stu-id="cceca-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="cceca-114">Mohu změnit číslo položky uvolněného produktu?</span><span class="sxs-lookup"><span data-stu-id="cceca-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="cceca-115">Ve většině případů nemůžete upravit čísla položek uvolněných produktů, protože tato změna způsobí poškození dat.</span><span class="sxs-lookup"><span data-stu-id="cceca-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="cceca-116">Číslo položky můžete upravit, pouze pokud musíte opravit poškození dat způsobené předchozím přejmenováním primárního klíče tohoto uvolněného produktu, jak je uvedeno v seznamu [odstraněných nebo zastaralých funkcí pro Finance and Operations 10.0.0 s aktualizací Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="cceca-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="cceca-117">Chcete-li mít možnost upravit čísla položek uvolněných produktů, [hlasujte pro tento nápad na portálu Nápady](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="cceca-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="cceca-118">Na řádku kusovníku se nezadává výchozí princip vyprazdňování z produktu.</span><span class="sxs-lookup"><span data-stu-id="cceca-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-119">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-119">Issue description</span></span>

<span data-ttu-id="cceca-120">Když přidáte položku do řádku kusovníku, systém nepoužívá výchozí informaci o zásadě vyprazdňování, která je pro položku nastavena.</span><span class="sxs-lookup"><span data-stu-id="cceca-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="cceca-121">Jinými slovy, princip vyprazdňování z položky se na stránce **Řádek kusovníku** nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="cceca-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-122">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-122">Issue resolution</span></span>

<span data-ttu-id="cceca-123">Pokud na řádku kusovníku určíte princip vyprazdňování, bude se vztahovat na tento řádek kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cceca-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="cceca-124">Pokud je však princip vyprazdňování prázdný nebo pokud není nastaven na řádku kusovníku, princip vyprazdňování nastavený na položce bude i nadále platit pro tento řádek kusovníku, i když se na řádku kusovníku nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="cceca-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="cceca-125">Výchozí logika pro další funkce v Microsoft Dynamics 365 Supply Chain Management obvykle tímto způsobem nefunguje.</span><span class="sxs-lookup"><span data-stu-id="cceca-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="cceca-126">Aktuální chování však nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="cceca-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="cceca-127">Jinak může dojít k porušení některých existujících přizpůsobení, které na to spoléhají.</span><span class="sxs-lookup"><span data-stu-id="cceca-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="cceca-128">Systém mi umožňuje uložit duplicitní čárové kódy pro různé položky nebo pro stejnou položku, která má různé dimenze.</span><span class="sxs-lookup"><span data-stu-id="cceca-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="cceca-129">Systém aktuálně nevynucuje jedinečné čárové kódy a přidání tohoto omezení by bylo zásadní změnou.</span><span class="sxs-lookup"><span data-stu-id="cceca-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="cceca-130">Microsoft má ve skutečnosti důkaz, že by tato změna narušila některé stávající instalace zákazníků.</span><span class="sxs-lookup"><span data-stu-id="cceca-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="cceca-131">Uvažujeme však o širší konstrukční změně, která tuto funkci v budoucnu povolí.</span><span class="sxs-lookup"><span data-stu-id="cceca-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="cceca-132">Při úpravě šablon záznamů položek se zobrazí následující chybová zpráva: „Nelze vytvořit umístění skladu, protože položka není na skladě.</span><span class="sxs-lookup"><span data-stu-id="cceca-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="cceca-133">Chcete-li zboží na skladě, je třeba vybrat možnost Skladovaný produkt ve skupině modelů přidružených položek.“</span><span class="sxs-lookup"><span data-stu-id="cceca-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-134">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-134">Issue description</span></span>

<span data-ttu-id="cceca-135">K tomuto problému dochází, pokud se pokusíte vytvořit šablonu pro položku, která není na skladě, pomocí těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="cceca-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="cceca-136">Otevřete uvolněný produkt, který není na skladě.</span><span class="sxs-lookup"><span data-stu-id="cceca-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="cceca-137">V podokně akcí na kartě **Možnosti** zvolte **Informace o záznamu**.</span><span class="sxs-lookup"><span data-stu-id="cceca-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="cceca-138">V dialogovém okně **Informace o záznamu** vyberte **Šablona firemních účtů**.</span><span class="sxs-lookup"><span data-stu-id="cceca-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="cceca-139">V tomto případě se zobrazí následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="cceca-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="cceca-140">Nelze vytvořit umístění ve skladu, protože položka není na skladě.</span><span class="sxs-lookup"><span data-stu-id="cceca-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="cceca-141">Chcete-li zboží na skladě, je třeba vybrat možnost Skladovaný produkt ve skupině modelů přidružených položek.</span><span class="sxs-lookup"><span data-stu-id="cceca-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-142">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-142">Issue resolution</span></span>

<span data-ttu-id="cceca-143">Proces vytváření šablon produktu vyžaduje zvláštní logiku specifickou pro produkt.</span><span class="sxs-lookup"><span data-stu-id="cceca-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="cceca-144">Proto pro tento účel nemůžete použít obecné tlačítko **Šablona účtů společnosti**.</span><span class="sxs-lookup"><span data-stu-id="cceca-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="cceca-145">Místo toho postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="cceca-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="cceca-146">Otevřete uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="cceca-146">Open a released product.</span></span>
1. <span data-ttu-id="cceca-147">V podokně akcí na kartě **Produkt** ve skupině **Nový** zvolte **Šablona \> Vytvořit sdílenou šablonu**.</span><span class="sxs-lookup"><span data-stu-id="cceca-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="cceca-148">Výchozí text nápovědy, který je přidán do atributů produktu, není v uvolněném produktu zadán.</span><span class="sxs-lookup"><span data-stu-id="cceca-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="cceca-149">Popis a text nápovědy, které jsou přidány do atributů produktu, nejsou ve uvolněných produktech viditelné nebo zadané ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="cceca-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="cceca-150">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="cceca-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="cceca-151">Výchozí množství, které se zadá, se liší, když je zaregistrováno z kusovníku a když je zaregistrováno z verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cceca-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-152">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-152">Issue description</span></span>

<span data-ttu-id="cceca-153">Ve výchozím nastavení, když přidáte položku do kusovníku, je množství nastaveno na 1 místo množství definovaného v poli **Min. objednané množství** na stránce **Výchozí nastavení objednávky** pro vybraný produkt.</span><span class="sxs-lookup"><span data-stu-id="cceca-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="cceca-154">Když však přidáte položku z verze kusovníku a vyberete položku a variantu, množství, které je zadáno ve výchozím nastavení, zohlední minimální množství, které je nastaveno ve výchozím nastavení objednávky pro konkrétní dimenze.</span><span class="sxs-lookup"><span data-stu-id="cceca-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-155">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-155">Issue resolution</span></span>

<span data-ttu-id="cceca-156">Toto chování se očekává.</span><span class="sxs-lookup"><span data-stu-id="cceca-156">This behavior is expected.</span></span> <span data-ttu-id="cceca-157">Skutečnost, že se logika liší v kusovníku a verzi kusovníku, je známým problémem.</span><span class="sxs-lookup"><span data-stu-id="cceca-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="cceca-158">Toto chování se nicméně nezmění, protože změna může ovlivnit mnoho různých scénářů zákazníků.</span><span class="sxs-lookup"><span data-stu-id="cceca-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="cceca-159">V podrobnostech o uvolněném produktu nemohu změnit připojené obrázky, které byly nahrány z datové entity Přílohy dokumentu produktu.</span><span class="sxs-lookup"><span data-stu-id="cceca-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-160">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-160">Issue description</span></span>

<span data-ttu-id="cceca-161">K tomuto problému může dojít, když připojíte obrázek k položce pomocí datová entita *Přílohy dokumentu produktu*.</span><span class="sxs-lookup"><span data-stu-id="cceca-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="cceca-162">V takovém případě se pro položku zobrazí obrázek položky.</span><span class="sxs-lookup"><span data-stu-id="cceca-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="cceca-163">Pokud však vyberete **Změnit obrázek**, v seznamu nahraných obrázků se nic nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="cceca-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="cceca-164">U položky se navíc nezobrazují žádné přílohy.</span><span class="sxs-lookup"><span data-stu-id="cceca-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-165">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-165">Issue resolution</span></span>

<span data-ttu-id="cceca-166">Entita *EcoResProductDocumentAttachmentEntity* (*Přílohy dokumentů produktu*) importuje přílohy dokumentů pro *produkty*, ale ne pro *uvolněné*.</span><span class="sxs-lookup"><span data-stu-id="cceca-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="cceca-167">(Uvolněné produkty jsou také známé jako *položky* .) Chcete-li zobrazit přílohy položky na stránce **Podrobnosti o uvolněném produktu**, musíte použít místo toho entitu *EcoResReleasedProductDocumentAttachmentEntity* (*Přílohy dokumentů uvolněného produktu*).</span><span class="sxs-lookup"><span data-stu-id="cceca-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="cceca-168">Konektor Microsoft Flow zobrazuje následující chybovou zprávu: „Aktualizace není povolena pro pole 'ProductNumber'.“</span><span class="sxs-lookup"><span data-stu-id="cceca-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-169">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-169">Issue description</span></span>

<span data-ttu-id="cceca-170">K tomuto problému dochází, pokud se pokusíte aktualizovat pole **Číslo produktu** pomocí entity V2 *Uvolněné produkty* a Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="cceca-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-171">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-171">Issue resolution</span></span>

<span data-ttu-id="cceca-172">Toto chování se očekává.</span><span class="sxs-lookup"><span data-stu-id="cceca-172">This behavior is expected.</span></span> <span data-ttu-id="cceca-173">Možnost upravovat číslo produktu uvolněného produktu byla odstraněna v Dynamics 365 Finance and Operations 10.0.0 s aktualizací Platform update 24, aby se zabránilo poškození dat.</span><span class="sxs-lookup"><span data-stu-id="cceca-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="cceca-174">Ve výjimečných případech, kdy musíte opravit poškození dat způsobené předchozím přejmenováním primárního klíče vydaného produktu, můžete požádat podporu Microsoftu, aby toto omezení dočasně odstranila.</span><span class="sxs-lookup"><span data-stu-id="cceca-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="cceca-175">Nemohu vytvořit uvolněnou variantu produktu v jiné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="cceca-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-176">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-176">Issue description</span></span>

<span data-ttu-id="cceca-177">Pokud se pokusíte uvolnit hlavní produkt bez variant a poté vytvořit varianty v každé právnické osobě (společnosti), jak jsou požadovány, nebudete moci uvolnit varianty pomocí návrhů variant.</span><span class="sxs-lookup"><span data-stu-id="cceca-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="cceca-178">Varianty také nebudete moci ručně vytvořit.</span><span class="sxs-lookup"><span data-stu-id="cceca-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-179">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-179">Issue resolution</span></span>

<span data-ttu-id="cceca-180">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="cceca-180">This behavior is by design.</span></span> <span data-ttu-id="cceca-181">Vztahy základního produktu a dimenze, které hlavní produkt může mít, jsou udržovány na sdílené úrovni.</span><span class="sxs-lookup"><span data-stu-id="cceca-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="cceca-182">Proto nemůžete vytvořit dostupné dimenze pro sdílený základní produkt v konkrétní právní entitě, kde jsou tyto dimenze uvolněny, a poté replikovat proces v každé právní entitě, kde jsou dimenze vyžadovány.</span><span class="sxs-lookup"><span data-stu-id="cceca-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="cceca-183">Místo toho musíte změnit proces uvolnění, abyste se přizpůsobili navrženému procesu.</span><span class="sxs-lookup"><span data-stu-id="cceca-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="cceca-184">Zde je proces uvolňování produktů.</span><span class="sxs-lookup"><span data-stu-id="cceca-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="cceca-185">Vytvořte sdílený základní produkt a dimenze, které lze uvolnit právnickým osobám.</span><span class="sxs-lookup"><span data-stu-id="cceca-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="cceca-186">Uvolněte produkty právnickým osobám buď pomocí návrhů variant, nebo ručním přidáním kombinací, které by měly být uvolněny.</span><span class="sxs-lookup"><span data-stu-id="cceca-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="cceca-187">Alternativně můžete přímo vytvořit uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="cceca-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="cceca-188">Když uvolním variantu v jiné společnosti, zobrazí se následující chybová zpráva: „Varianta produktu se zadanými dimenzemi již byla vytvořena.“</span><span class="sxs-lookup"><span data-stu-id="cceca-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cceca-189">Popis problému</span><span class="sxs-lookup"><span data-stu-id="cceca-189">Issue description</span></span>

<span data-ttu-id="cceca-190">Pokud již byla ve společnosti A uvolněna varianta produktu a pokusíte se ji ve společnosti B uvolnit pomocí tlačítka **Nový** na stránce **Uvolněné varianty produktu**, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="cceca-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="cceca-191">Varianta produktu s určenými dimenzemi již byla vytvořena.</span><span class="sxs-lookup"><span data-stu-id="cceca-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cceca-192">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="cceca-192">Issue resolution</span></span>

<span data-ttu-id="cceca-193">Tlačítko **Nový** na stránce **Uvolněné varianty produktu** vytvoří variantu a uvolní ji v kontextu společnosti.</span><span class="sxs-lookup"><span data-stu-id="cceca-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="cceca-194">Pokud již byla varianta vytvořena, nemůžete použít tlačítko **Nový** pro uvolnění v jiné společnosti.</span><span class="sxs-lookup"><span data-stu-id="cceca-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="cceca-195">Chcete-li problém vyřešit, otevřete stránku **Základní produkt** a vyberte **Uvolnit produkt** pro uvolnění stávající varianty v požadované společnosti.</span><span class="sxs-lookup"><span data-stu-id="cceca-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]