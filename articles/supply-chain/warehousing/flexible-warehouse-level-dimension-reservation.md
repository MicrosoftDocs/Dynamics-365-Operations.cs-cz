---
title: Flexibilní zásada rezervace dimenze na úrovni skladu
description: V tomto tématu jsou popsány zásady rezervace zásob, které umožňují společnostem prodávat produkty sledované podle dávky a spustit jejich logistiku, protože operace s povoleným WMS rezervují konkrétní dávky pro prodejní objednávky zákazníka, a to i v případě, že hierarchie rezervací, přidružená k produktům, neumožňuje rezervaci specifických dávek.
author: omulvad
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c0baf96315dd9fe6bc1984d337fd1c50ae47016a
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031036"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="8e47c-103">Flexibilní zásada rezervace dimenze na úrovni skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e47c-104">Pokud je hierarchie rezervací zásob typu Batch-below\[location\] spojena s produkty, podniky, které prodávají produkty sledované podle dávky a spouštějí své logistiku jako operace, které jsou povoleny pro Microsoft Dynamics 365 Warehouse Management System (WMS), nemohou rezervovat konkrétní dávky těchto produktů pro prodejní objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="8e47c-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="8e47c-105">V tomto tématu jsou popsány zásady rezervace zásob, které těmto podnikům umožňují rezervovat specifické dávky, a to i v případě, že jsou produkty přiřazeny k hierarchii rezervací Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="8e47c-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="8e47c-106">Hierarchie rezervací zásob</span><span class="sxs-lookup"><span data-stu-id="8e47c-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="8e47c-107">V tomto oddílu je shrnuta existující hierarchie rezervací zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="8e47c-108">Zaměřuje se na způsob, jakým je nakládáno s položkami sledovanými dávkou a sériovým číslem.</span><span class="sxs-lookup"><span data-stu-id="8e47c-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="8e47c-109">Hierarchie rezervace zásob určuje, že pokud se jedná o dimenze uskladnění, objednávka poptávky nese povinné dimenze pracoviště, skladu a stavu zásob, zatímco logika skladu je odpovědná za přiřazení skladového místa k požadovanému množství a rezervaci skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="8e47c-110">Jinak řečeno, v interakcích mezi objednávkou poptávky a skladovými operacemi se očekává, že objednávka poptávky indikuje, odkud musí být objednávka expedována (tj. pracoviště a sklad).</span><span class="sxs-lookup"><span data-stu-id="8e47c-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="8e47c-111">Sklad pak spoléhá na svou logiku k nalezení požadovaného množství v skladových prostorách.</span><span class="sxs-lookup"><span data-stu-id="8e47c-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="8e47c-112">Chcete-li však zohlednit provozní model podniku, je sledovací dimenze (dávka a sériová čísla) předmětem větší flexibility.</span><span class="sxs-lookup"><span data-stu-id="8e47c-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="8e47c-113">Hierarchie rezervací zásob může vyhovovat situacím, pro které platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="8e47c-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="8e47c-114">Podnik spoléhá na své skladové operace za účelem správy výdeje množství, která mají čísla dávek nebo sériová čísla po nalezení množství v prostoru úložiště skladu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="8e47c-115">Tento model se často označuje jako *Batch-below\[location\]*.</span><span class="sxs-lookup"><span data-stu-id="8e47c-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="8e47c-116">Obvykle se používá v případě, že identifikace dávky nebo sériového čísla produktu není důležitá pro zákazníky, kteří učiní poptávku u prodávající společnosti.</span><span class="sxs-lookup"><span data-stu-id="8e47c-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="8e47c-117">Pokud jsou dávka a sériová čísla součástí specifikace objednávky odběratele a jsou zaznamenána na objednávce poptávky, skladové operace, které vyhledají množství ve skladu, jsou omezeny konkrétními požadovanými počty a nejsou povoleny jejich změny.</span><span class="sxs-lookup"><span data-stu-id="8e47c-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="8e47c-118">Tento model se označuje jako *Batch-above\[location\]*.</span><span class="sxs-lookup"><span data-stu-id="8e47c-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="8e47c-119">V těchto scénářích je výzvou, že každému uvolněnému produktu lze přiřadit pouze jednu hierarchii rezervace zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="8e47c-120">Proto, aby WMS zpracoval sledované položky, poté, co v přiřazení hierarchie určí, kdy má být provedena rezervace dávky nebo sériového čísla (buď při objednávce poptávky nebo při zahájení práce výdeje skladu), toto časování nelze změnit ad hoc.</span><span class="sxs-lookup"><span data-stu-id="8e47c-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="8e47c-121">Pružná rezervace pro položky sledované dávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="8e47c-122">Scénáře obchodu</span><span class="sxs-lookup"><span data-stu-id="8e47c-122">Business scenario</span></span>

<span data-ttu-id="8e47c-123">V tomto scénáři společnost používá strategii zásob, při které je dokončené zboží sledováno pomocí čísel dávek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="8e47c-124">Tato společnost také používá pracovní vytížení WHS.</span><span class="sxs-lookup"><span data-stu-id="8e47c-124">This company also uses the WHS workload.</span></span> <span data-ttu-id="8e47c-125">Vzhledem k tomu, že toto pracovní vytížení má dobře vybavenou logiku pro plánování a provádění operací výdeje a expedice skladu pro položky s povolenou dávkou, je většina dokončených položek přidružena k hierarchii rezervací zásob "Batch-below\[location\]".</span><span class="sxs-lookup"><span data-stu-id="8e47c-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="8e47c-126">Výhodou tohoto typu operačního nastavení je to, že rozhodnutí (což jsou ve skutečnosti rozhodnutí o rezervacích) o tom, které dávky vyskladnit a do jakého skladu je vložit, budou odloženy až do zahájení operace výdeje skladu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="8e47c-127">Nejsou provedeny při učinění objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="8e47c-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="8e47c-128">Ačkoliv hierarchie rezervací Batch-below\[location\] slouží k zajištění správných obchodních cílů společnosti, mnoho zavedených zákazníků společnosti vyžaduje stejnou dávku, při které byly tyto produkty zakoupeny dříve.</span><span class="sxs-lookup"><span data-stu-id="8e47c-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="8e47c-129">Z toho vyplývá, že společnost hledá flexibilitu ve způsobu, jakým jsou zpracovávána pravidla rezervace dávky, takže v závislosti na poptávce odběratelů po stejné položce dojde k následujícímu chování:</span><span class="sxs-lookup"><span data-stu-id="8e47c-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="8e47c-130">Číslo dávky lze zaznamenat a rezervovat, když je objednávka provedena, zpracovatelem prodeje, a nelze ji změnit během skladových operací anebo pořídit jinými požadavky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="8e47c-131">Toto chování pomáhá zaručit, že objednané číslo dávky je expedováno odběrateli.</span><span class="sxs-lookup"><span data-stu-id="8e47c-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="8e47c-132">Není-li číslo dávky pro odběratele důležité, skladové operace mohou určit číslo dávky během výdejní práce po provedení registrace prodejní objednávky a rezervace.</span><span class="sxs-lookup"><span data-stu-id="8e47c-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="8e47c-133">Povolení rezervace konkrétní dávky v prodejní objednávce</span><span class="sxs-lookup"><span data-stu-id="8e47c-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="8e47c-134">Chcete-li přizpůsobit požadovanou flexibilitu v chování rezervace dávek u položek, které jsou přidruženy k hierarchii rezervace zásob Batch-below\[location\], musí manažeři zásob zaškrtnout políčko **Povolit rezervaci na objednávce poptávky** pro úroveň **čísla dávky** na stránce **hierarchie rezervací zásob**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Zflexibilnění hierarchie rezervace zásob](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="8e47c-136">Je- li vybrána úroveň **čísla dávky** v hierarchii, budou automaticky vybrány všechny dimenze nad úrovní a až k úrovni **skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="8e47c-137">(Ve výchozím nastavení jsou přednastaveny všechny dimenze nad úrovní **skladového místa**.) Toto chování odpovídá logice, kde jsou všechny dimenze v rozsahu mezi číslem dávky a místem automaticky rezervovány po rezervaci konkrétního čísla dávky na řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="8e47c-138">Zaškrtávací políčko **Povolit rezervaci na objednávce poptávky** se vztahuje pouze na úrovně hierarchie rezervací, které jsou pod dimenzí skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="8e47c-139">**Číslo dávky** je jediná úroveň v hierarchii, která je otevřená pro zásadu pružné rezervace.</span><span class="sxs-lookup"><span data-stu-id="8e47c-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="8e47c-140">Jinými slovy, pro úroveň **umístění**, **registrační značky** nebo **sériového čísla** nelze zaškrtnout políčko **Povolit rezervaci na objednávce poptávky**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="8e47c-141">Pokud hierarchie rezervace obsahuje dimenzi sériového čísla (která musí vždy být nižší než úroveň **Číslo dávky**) a pokud jste pro číslo dávky aktivovali rezervaci specifickou pro dávku, systém bude pokračovat ve zpracování rezervací sériových čísel a operací výdeje na základě pravidel, která platí pro zásadu rezervace Serial-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="8e47c-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="8e47c-142">V kterémkoli bodě můžete povolit rezervaci specifickou pro dávku pro existující hierarchii rezervací Batch-below\[location\] v rámci vašeho nasazení.</span><span class="sxs-lookup"><span data-stu-id="8e47c-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="8e47c-143">Tato změna neovlivní žádné rezervace a otevřené práce skladu, které byly vytvořeny před provedením změny.</span><span class="sxs-lookup"><span data-stu-id="8e47c-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="8e47c-144">Zaškrtnutí políčka **Povolit rezervaci na objednávce poptávky** však nelze odstranit, pokud pro jednu nebo více položek které jsou přidruženy k dané hierarchii rezervací, existují transakce zásob typů výdeje **Rezervované objednané**, **Rezervované – fyzicky**, nebo **Objednáno**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="8e47c-145">Pokud existující hierarchie rezervací položky nepovoluje dávkovou specifikaci pro objednávku, můžete ji přiřadit k hierarchii rezervací, která povoluje specifikaci dávky, pokud je struktura úrovně hierarchie v obou hierarchiích stejná.</span><span class="sxs-lookup"><span data-stu-id="8e47c-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="8e47c-146">Použijte funkci **Změnit hierarchii rezervací pro položky** pro provedení opětovného přiřazení.</span><span class="sxs-lookup"><span data-stu-id="8e47c-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="8e47c-147">Tato změna může být důležitá v případě, že chcete zabránit flexibilní rezervaci dávky pro podmnožinu položek sledovaných dávkou, ale povolit ji pro zbytek portfolia produktů.</span><span class="sxs-lookup"><span data-stu-id="8e47c-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="8e47c-148">Bez ohledu na to, zda jste zaškrtli políčko **Povolit rezervaci na objednávce poptávky**, nechcete-li rezervovat určité číslo dávky pro položku na řádku objednávky, bude stále platit výchozí logika skladového místa, která je platná pro hierarchii rezervace Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="8e47c-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="8e47c-149">Rezervace konkrétního čísla dávky pro objednávku odběratele</span><span class="sxs-lookup"><span data-stu-id="8e47c-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="8e47c-150">Po nastavení hierarchie rezervací zásob Batch-below\[location\] pro položku sledovanou dávkou za účelem umožnění rezervace konkrétních čísel dávky na prodejních objednávkách mohou zpracovatelé prodejní objednávky provést objednávky odběratele pro stejnou položku jedním z následujících způsobů:</span><span class="sxs-lookup"><span data-stu-id="8e47c-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="8e47c-151">**Zadat podrobnosti objednávky bez zadání čísla dávky** – tento přístup by měl být použit v případě, že specifikace dávky produktu není pro odběratele důležitá.</span><span class="sxs-lookup"><span data-stu-id="8e47c-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="8e47c-152">Všechny existující procesy související se zpracováním objednávky tohoto typu v systému zůstanou nezměněny.</span><span class="sxs-lookup"><span data-stu-id="8e47c-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="8e47c-153">Na straně uživatelů nejsou vyžadovány žádné další úvahy.</span><span class="sxs-lookup"><span data-stu-id="8e47c-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="8e47c-154">**Zadat podrobnosti objednávky a rezervovat určité číslo dávky** – tento přístup by měl být použit v případě, že odběratel požaduje určitou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="8e47c-155">Zákazníci obvykle požadují určitou dávku při opětovném objednání produktu, který dříve nakoupili.</span><span class="sxs-lookup"><span data-stu-id="8e47c-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="8e47c-156">Tento typ rezervace specifické pro dávku se nazývá *rezervace potvrzená objednávkou*.</span><span class="sxs-lookup"><span data-stu-id="8e47c-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="8e47c-157">Následující sada pravidel je platná při zpracování množství a číslo dávky je potvrzeno pro specifickou objednávku:</span><span class="sxs-lookup"><span data-stu-id="8e47c-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="8e47c-158">Chcete-li povolit rezervaci určitého čísla dávky pro položku pod zásadami rezervace Batch-below\[location\], musí systém rezervovat všechny dimenze v rámci skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="8e47c-159">Tento rozsah obvykle zahrnuje dimenzi registrační značky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="8e47c-160">Směrnice skladových míst se nepoužívají, pokud je pro řádek prodeje vytvořena výdejní práce, která používá rezervaci dávky potvrzenou objednávkou.</span><span class="sxs-lookup"><span data-stu-id="8e47c-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="8e47c-161">Během zpracování práce skladu pro dávky potvrzené objednávkou nemůže uživatel ani systém změnit číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="8e47c-162">(Toto zpracování zahrnuje zpracování výjimek.)</span><span class="sxs-lookup"><span data-stu-id="8e47c-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="8e47c-163">Následující příklad ukazuje celý tok.</span><span class="sxs-lookup"><span data-stu-id="8e47c-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="8e47c-164">Příklad</span><span class="sxs-lookup"><span data-stu-id="8e47c-164">Example scenario</span></span>

<span data-ttu-id="8e47c-165">Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="8e47c-166">Nastavení hierarchie rezervací zásob, aby byla povolena rezervace specifická pro dávku</span><span class="sxs-lookup"><span data-stu-id="8e47c-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="8e47c-167">Přejděte na **Řízení skladu** \> **Nastavení** \> **Zásoby \> Hierarchie rezervací**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="8e47c-168">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-168">Select **New**.</span></span>
3. <span data-ttu-id="8e47c-169">Do pole **Název** zadejte název (například **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="8e47c-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="8e47c-170">Do pole **Popis** zadejte popis (například **Batch below flexible**).</span><span class="sxs-lookup"><span data-stu-id="8e47c-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="8e47c-171">V poli **Vybrané** zvolte **Sériové číslo** a **Vlastník** a poté zvolte tlačítko šipky doleva pro přesun na pole **K dipozici**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="8e47c-172">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-172">Select **OK**.</span></span>
7. <span data-ttu-id="8e47c-173">V řádku pro úroveň dimenze **Číslo dávky** zaškrtněte políčko **Povolit rezervaci na objednávce poptávky**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="8e47c-174">Úrovně **Registrační značka** a **Skladové místo** jsou vybrány automaticky a nelze u nich zrušit zaškrtávací políčko.</span><span class="sxs-lookup"><span data-stu-id="8e47c-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="8e47c-175">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="8e47c-176">Vytvoření nového uvolněného produktu</span><span class="sxs-lookup"><span data-stu-id="8e47c-176">Create a new released product</span></span>

1. <span data-ttu-id="8e47c-177">Pomocí těchto hodnot nastavíte tři základní datové parametry produktu:</span><span class="sxs-lookup"><span data-stu-id="8e47c-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="8e47c-178">V poli **Skupina dimenze úložiště** vyberte **Ware**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="8e47c-179">V poli **Skupina sledovací dimenze** vyberte **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="8e47c-180">V poli **Hierarchie rezervace** vyberte **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="8e47c-181">Vytvořte dvě čísla dávek, jako například **B11** a **B22**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="8e47c-182">Přidejte množství položek k zásobám na skladě pomocí následujících hodnot.</span><span class="sxs-lookup"><span data-stu-id="8e47c-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="8e47c-183">Sklad</span><span class="sxs-lookup"><span data-stu-id="8e47c-183">Warehouse</span></span> | <span data-ttu-id="8e47c-184">Číslo dávky</span><span class="sxs-lookup"><span data-stu-id="8e47c-184">Batch number</span></span> | <span data-ttu-id="8e47c-185">Umístění</span><span class="sxs-lookup"><span data-stu-id="8e47c-185">Location</span></span> | <span data-ttu-id="8e47c-186">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="8e47c-186">License plate</span></span> | <span data-ttu-id="8e47c-187">Množství</span><span class="sxs-lookup"><span data-stu-id="8e47c-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="8e47c-188">24</span><span class="sxs-lookup"><span data-stu-id="8e47c-188">24</span></span>        | <span data-ttu-id="8e47c-189">B11</span><span class="sxs-lookup"><span data-stu-id="8e47c-189">B11</span></span>          | <span data-ttu-id="8e47c-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="8e47c-190">BULK-001</span></span> | <span data-ttu-id="8e47c-191">Žádní</span><span class="sxs-lookup"><span data-stu-id="8e47c-191">None</span></span>          | <span data-ttu-id="8e47c-192">10</span><span class="sxs-lookup"><span data-stu-id="8e47c-192">10</span></span>       |
    | <span data-ttu-id="8e47c-193">24</span><span class="sxs-lookup"><span data-stu-id="8e47c-193">24</span></span>        | <span data-ttu-id="8e47c-194">B11</span><span class="sxs-lookup"><span data-stu-id="8e47c-194">B11</span></span>          | <span data-ttu-id="8e47c-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="8e47c-195">FL-001</span></span>   | <span data-ttu-id="8e47c-196">LP11</span><span class="sxs-lookup"><span data-stu-id="8e47c-196">LP11</span></span>          | <span data-ttu-id="8e47c-197">10</span><span class="sxs-lookup"><span data-stu-id="8e47c-197">10</span></span>       |
    | <span data-ttu-id="8e47c-198">24</span><span class="sxs-lookup"><span data-stu-id="8e47c-198">24</span></span>        | <span data-ttu-id="8e47c-199">B22</span><span class="sxs-lookup"><span data-stu-id="8e47c-199">B22</span></span>          | <span data-ttu-id="8e47c-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="8e47c-200">FL-002</span></span>   | <span data-ttu-id="8e47c-201">LP22</span><span class="sxs-lookup"><span data-stu-id="8e47c-201">LP22</span></span>          | <span data-ttu-id="8e47c-202">10</span><span class="sxs-lookup"><span data-stu-id="8e47c-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="8e47c-203">Zadání podrobností prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="8e47c-203">Enter sales order details</span></span>

1. <span data-ttu-id="8e47c-204">Přejděte na **Prodej a marketing** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="8e47c-205">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-205">Select **New**.</span></span>
3. <span data-ttu-id="8e47c-206">V záhlaví prodejní objednávky v poli **Účet odběratele** zadejte **US-003**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="8e47c-207">Přidejte řádek pro novou položku a jako množství zadejte **10**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="8e47c-208">Ujistěte se, že je v poli **Sklad** nastavena hodnota na **24**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="8e47c-209">Na záložce s náhledem **Řádky prodejní objednávky** vyberte možnost **Zásoby** a poté ve skupině **Udržovat** vyberte možnost **Rezervace dávky**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="8e47c-210">Stránka **Rezervace dávky** zobrazí seznam dávek, které jsou k dispozici pro rezervaci pro daný řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="8e47c-211">V tomto příkladu se zobrazí množství **20** pro číslo dávky **B11** a množství **10** pro číslo dávky **B22**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="8e47c-212">Všimněte si, ke stránce **Rezervace dávky** nelze získat přístup z řádku, pokud je položka na tomto řádku přidružena k hierarchii rezervace Batch-below\[location\] v případě, že není nastavena tak, aby umožňovala rezervaci specifickou pro dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e47c-213">Chcete-li rezervovat určitou dávku pro prodejní objednávku, je nutné použít stránku **Rezervace dávky**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="8e47c-214">Zadáte-li číslo dávky přímo do řádku prodejní objednávky, systém se bude chovat, jako byste zadali konkrétní hodnotu dávky pro položku, na kterou se vztahuje zásada rezervace Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="8e47c-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="8e47c-215">Po uložení řádku se zobrazí varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="8e47c-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="8e47c-216">Pokud potvrdíte, že číslo dávky by mělo být zadáno přímo na řádku objednávky, řádek nebude zpracován běžnou logikou správy skladu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="8e47c-217">Pokud rezervujete množství na stránce **Rezervace**, žádná specifická dávka nebude rezervována a provedení skladových operací pro tento řádek bude následovat pravidla aplikovatelná pod zásadami rezervace Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="8e47c-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="8e47c-218">Tato stránka obecně funguje a je v interakci stejným způsobem, jako pracuje a je závislá na položkách, které mají přidruženou hierarchii rezervací typu Batch-above\[location\].</span><span class="sxs-lookup"><span data-stu-id="8e47c-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="8e47c-219">Platí však následující výjimky:</span><span class="sxs-lookup"><span data-stu-id="8e47c-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="8e47c-220">Záložka s náhledem **Čísla dávek potvrzená pro řádek zdroje** zobrazí čísla dávek, která jsou vyhrazena pro řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="8e47c-221">Hodnoty dávky v mřížce se zobrazí v průběhu cyklu splnění řádku objednávky včetně fází zpracování skladu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="8e47c-222">Naopak na záložce s náhledem **Přehled** je běžná rezervace řádku objednávky (tj. rezervace, která se provádí pro dimenze nad úrovní **skladového místa**), v mřížce zobrazena až do bodu vytvoření skladové práce.</span><span class="sxs-lookup"><span data-stu-id="8e47c-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="8e47c-223">Entita práce pak převezme rezervaci řádku a na stránce se již nebude zobrazovat rezervace řádku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="8e47c-224">Záložka s náhledem **Čísla dávek potvrzená pro řádek zdroje** pomáhá zajistit, že procesor prodejní objednávky může zobrazit čísla dávek, která byla potvrzena do objednávky zákazníka v kterémkoli okamžiku během svého životního cyklu, až do fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e47c-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="8e47c-225">Kromě rezervace konkrétní dávky může uživatel ručně vybrat konkrétní místo dávky a registrační značku namísto toho, aby je systém vybral automaticky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="8e47c-226">Tato schopnost souvisí s návrhem mechanismu rezervace dávky potvrzené objednávkou.</span><span class="sxs-lookup"><span data-stu-id="8e47c-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="8e47c-227">Jak bylo zmíněno dříve, chcete-li povolit rezervaci určitého čísla dávky pro položku pod zásadami rezervace Batch-below\[location\], musí systém rezervovat všechny dimenze v rámci skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="8e47c-228">Skladová práce proto bude mít stejné dimenze uskladnění, které byly rezervovány uživateli, kteří pracovali s objednávkami, a nemusí vždy představovat umístění úložiště položek, které je pro operace výdeje vhodné nebo dokonce možné.</span><span class="sxs-lookup"><span data-stu-id="8e47c-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="8e47c-229">Pokud zpracovatelé objednávek vědí o omezeních skladu, mohou chtít ručně vybrat určitá skladová místa a registrační značky při rezervaci dávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="8e47c-230">V takovém případě musí uživatel použít funkci **Zobrazit dimenze** v záhlaví stránky a přidat umístění a registrační značku do mřížky na záložce s náhledem **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="8e47c-231">Na stránce **Rezervace dávky** vyberte řádek pro dávku **B11** a pak vyberte **Řádek rezervace**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="8e47c-232">V průběhu automatické rezervace není určena žádná logika pro přiřazování skladových míst a registračních značek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="8e47c-233">Množství lze ručně zadat do pole **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="8e47c-234">Všimněte si, že na záložce s náhledem **Čísla dávek potvrzená pro řádek zdroje** se zobrazí dávka **B11** jako **Potvrzená**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Potvrzení konkrétního čísla dávky na řádek prodejní objednávky na stránce rezervace dávky](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="8e47c-236">Rezervaci množství na řádku prodejní objednávky lze provést ve více dávkách.</span><span class="sxs-lookup"><span data-stu-id="8e47c-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="8e47c-237">Stejně tak lze provést rezervaci stejné dávky proti několika místům a registračním značkám (pokud jsou pro skladová místa povoleny registrační značky).</span><span class="sxs-lookup"><span data-stu-id="8e47c-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="8e47c-238">Rezervace konkrétní dávky pro množství na řádku prodejní objednávky může být také částečná.</span><span class="sxs-lookup"><span data-stu-id="8e47c-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="8e47c-239">Například celkové množství 100 jednotek může být rezervováno tak, aby určitá dávka byla potvrzena na 20 jednotek, zatímco 80 jednotek je rezervováno na pracovišti a na úrovni skladů pro všechny dostupné dávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="8e47c-240">V tomto případě bude WMS zpracovávat operace výdeje pomocí dvou oddělených řádků práce.</span><span class="sxs-lookup"><span data-stu-id="8e47c-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="8e47c-241">Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="8e47c-242">Vyberte položku a poté vyberte **Spravovat zásoby** \> **Zobrazení** \> **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Rezervace potvrzená objednávkou jako typ skladové transakce](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="8e47c-244">Zkontrolujte skladové transakce položky, které souvisejí s rezervací řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="8e47c-245">Transakce, ve které je pole **Odkaz** nastaveno na **Prodejní objednávka** a pole **Výdej** je nastaveno **Rezervované – fyzicky** představuje rezervaci řádku objednávky pro dimenze zásob nad úrovní **skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="8e47c-246">Podle hierarchie rezervací zásob položky jsou tyto dimenze pracoviště, sklad a stav zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="8e47c-247">Transakce, ve které je pole **Odkaz** nastaveno na **Rezervace potvrzená objednávkou** a pole **Výdej** je nastaveno **Rezervované – fyzicky** představuje rezervaci řádku objednávky pro specifickou dávku a pro všechny dimenze zásob nad ní.</span><span class="sxs-lookup"><span data-stu-id="8e47c-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="8e47c-248">Podle hierarchie rezervací zásob položky jsou tyto dimenze číslo dávky a skladové místo.</span><span class="sxs-lookup"><span data-stu-id="8e47c-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="8e47c-249">V tomto příkladu je skladové místo **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="8e47c-250">V záhlaví prodejní objednávky vyberte **Sklad** \> **Akce** \> **Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="8e47c-251">Řádek objednávky je nyní ve vlně a vytvoří se vytížení a práce.</span><span class="sxs-lookup"><span data-stu-id="8e47c-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="8e47c-252">Kontrola a zpracování práci skladu s čísly dávek potvrzených objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="8e47c-253">Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad** \> **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="8e47c-254">Práce, která zpracovává operaci výdeje pro množství dávky potvrzené v řádku prodejní objednávky, má následující charakteristiky:</span><span class="sxs-lookup"><span data-stu-id="8e47c-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="8e47c-255">Chcete-li vytvořit práci, systém použije šablony práce, ale ne směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="8e47c-256">Chcete-li určit, kdy má být vytvořena nová práce, bude použito standardní nastavení definované pro šablony práce, jako je například maximální počet řádků výdeje nebo určitá měrná jednotka.</span><span class="sxs-lookup"><span data-stu-id="8e47c-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="8e47c-257">Pravidla, která jsou spojena se směrnicemi skladových míst pro určení skladových místa výdeje, však nejsou zvažována, protože rezervace potvrzená objednávkou již určuje všechny dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="8e47c-258">Tyto dimenze zásob obsahují dimenze na úrovni skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="8e47c-259">Tato práce tedy tyto dimenze zdědí bez nutnosti konzultovat směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="8e47c-260">Číslo dávky není zobrazeno na řádku výdeje (jako je například případ pro řádek práce vytvořený pro položku, která má přidruženou hierarchii rezervace Batch-above\[location\].) Místo toho se v poli "od" číslo dávky a všechny ostatní dimenze uskladnění zobrazí na skladové transakci řádku práce, která je odkazována z přidružených skladových transakcí.</span><span class="sxs-lookup"><span data-stu-id="8e47c-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Skladová transakce pro práci, která pochází z rezervace potvrzené objednávkou](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="8e47c-262">Po vytvoření práce se skladová transakce položky, kde je pole **Odkaz** nastaveno na **Rezervace potvrzená objednávkou**, odstraní.</span><span class="sxs-lookup"><span data-stu-id="8e47c-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="8e47c-263">Skladová transakce, kde je pole **Odkaz** nastaveno na **Práce**, nyní ukládá fyzickou rezervaci ve všech dimenzích zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="8e47c-264">Skladové operace mohou pokračovat v provádění práce obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="8e47c-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="8e47c-265">Pokyny v mobilním zařízení však nařídí pracovníkovi, aby vydával určité číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="8e47c-266">V prostředích skladu, kde jsou skladová místa řízena registrační značkou, poté, co pracovník dostane do skladového místa, kde je uložena stejná dávka na více registračních štítků, může vybírat z libovolné registrační značky, která ještě není rezervována (například jinou rezervace nebo práce potvrzené objednávkou, která pochází z rezervace daného typu.)</span><span class="sxs-lookup"><span data-stu-id="8e47c-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="8e47c-267">Pokud z místa uvedeného na řádku práce odcházíte k vyskladnění, mohou operátoři skladu použít jednu z následujících akcí, které přesměrují výběr konkrétní dávky z vhodnějšího umístění:</span><span class="sxs-lookup"><span data-stu-id="8e47c-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="8e47c-268">Standardní akce **Přepsat umístění** na mobilním zařízení (za předpokladu, že je nastavení **Umožnit přepis výdejního umístění** pracovníka skladu povoleno)</span><span class="sxs-lookup"><span data-stu-id="8e47c-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="8e47c-269">Akce **Změnit umístění** na stránce **Podrobnosti seznamu práce**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="8e47c-270">V mobilním zařízení dokončete výdej a vklad práce.</span><span class="sxs-lookup"><span data-stu-id="8e47c-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="8e47c-271">Množství **10** pro číslo dávky **B11** je nyní vyskladněno pro řádek prodejní objednávky a je vloženo do umístění **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="8e47c-272">V tomto okamžiku je vše připraveno k naložení na nákladní vůz a odesláno na adresu odběratele.</span><span class="sxs-lookup"><span data-stu-id="8e47c-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="8e47c-273">Zpracování výjimky práce skladu s čísly dávek potvrzených objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="8e47c-274">Práce na skladě pro výdej čísel dávek potvrzených objednávkou podléhá stejnému standardnímu zpracování výjimek a akcím při běžné práci.</span><span class="sxs-lookup"><span data-stu-id="8e47c-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="8e47c-275">Obecně platí, že otevřenou práci nebo řádek práce lze zrušit, lze je přerušit, protože skladovací místo uživatele je plné, může být krátkodobě vyskladněno a je aktualizovat z důvodu přesunu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="8e47c-276">Stejně tak lze snížit vyskladněné množství práce, které již bylo dokončeno, nebo lze stornovat práci.</span><span class="sxs-lookup"><span data-stu-id="8e47c-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="8e47c-277">Následující pravidlo klíče se použije na všechny tyto akce zpracování výjimek: číslo dávky, které bylo rezervováno pro odběratele, nelze nikdy nahradit jiným číslem dávky, ale dimenze uskladnění (umístění a registrační značka) mohou být změněny buď pomocí Ruční aktualizace uživatelem nebo automatickou aktualizací systémem.</span><span class="sxs-lookup"><span data-stu-id="8e47c-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="8e47c-278">Automatická aktualizace je založena na stejném náhodném přiřazení dimenzí úložiště, které byly použity, když byla určitá dávka automaticky rezervována, ale nebyly zadány žádné dimenze úložiště.</span><span class="sxs-lookup"><span data-stu-id="8e47c-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="8e47c-279">Příklad</span><span class="sxs-lookup"><span data-stu-id="8e47c-279">Example scenario</span></span>

<span data-ttu-id="8e47c-280">Příkladem tohoto scénáře je situace, kdy je dříve dokončená práce vyzvednuta pomocí funkce **Snížit vyskladněné množství**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="8e47c-281">Tento příklad pokračuje v předchozím příkladu v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="8e47c-282">Přejděte na **Řízení skladu** \> **Nakládky** \> **Aktivní nakládky**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="8e47c-283">Vyberte nakládku, která byla vytvořena v souvislosti s dodávkou prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="8e47c-284">Na záložce s náhledem **Naložit řádky objednávky** zvolte **Snížit vyskladněné množství**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="8e47c-285">Na stránce **Snížit vyskladněné množství** vyberte v poli **Přesunout na místo** možnost **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="8e47c-286">V poli **Přejít na registrační značku** zvolte **LP33**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="8e47c-287">V mřížce v poli **Skladové množství ke zrušení výdeje** zadejte **10**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="8e47c-288">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-288">Select **OK**.</span></span>

<span data-ttu-id="8e47c-289">Zde jsou výsledky akce zrušení výdeje:</span><span class="sxs-lookup"><span data-stu-id="8e47c-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="8e47c-290">Stav dříve uzavřené práce je nastaven na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="8e47c-291">Nová práce typu **Přesun zásob** se vytvoří pro nevyzvednuté množství **10** pro číslo dávky **B11**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="8e47c-292">Tato práce představuje přesun z místa **Baydoor** na registrační značku **LP33** v umístění **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="8e47c-293">Stav je nastaven na **Zavřeno**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="8e47c-294">Systém znovu rezervuje číslo dávky, které bylo původně objednáno, a přiřadí ID umístění a registrační značky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="8e47c-295">(Tento proces odpovídá spuštění funkce **Rezervovat řádek** pro řádek objednávky pro dané číslo dávky).</span><span class="sxs-lookup"><span data-stu-id="8e47c-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="8e47c-296">Výsledkem je, že se dávka **B11** zobrazí jako potvrzená na záložce s náhledem **Čísla dávek potvrzená pro řádek zdroje** na stránce **Rezervace dávky**, a pole **Rezervace** obsahuje množství **10** pro číslo dávky **B11**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="8e47c-297">Dále je pole **Místo** nastaveno na **FL-001** a pole **Registrační značka** je nastaveno na **LP11**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="8e47c-298">(Tato pole můžete přidat do mřížky, pokud nejsou viditelná.)</span><span class="sxs-lookup"><span data-stu-id="8e47c-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="8e47c-299">V následujících tabulkách je uveden přehled, který zobrazuje způsob, jakým systém zpracovává rezervace dávky potvrzené objednávkou pro určité akce skladu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="8e47c-300">Chcete-li interpretovat obsah v tabulkách, předpokládejme, že každá akce skladu je spuštěna v kontextu existující práce ve skladu, která pochází z rezervace dávky potvrzené objednávkou, nebo že provádění jednotlivých akcí skladu ovlivňuje práci tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="8e47c-301">V těchto tabulkách sloupec "množství dávky je k dispozici" označuje, zda množství dávky k dispozici kromě množství, které již bylo rezervováno pro aktuální potvrzené rezervace nebo již rezervované pro práci ve skladu pochází z rezervací daného typu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="8e47c-302">Přepsání místa výdeje na otevřené práci</span><span class="sxs-lookup"><span data-stu-id="8e47c-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-303">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-304">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-305">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-305">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-306">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-306">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-307">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-308">Možnost <strong>Umožnit přepis výdejního umístění</strong> je povolena na pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="8e47c-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="8e47c-309">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-310">Vyberte položku nabídky <strong>Přepsat umístění</strong> v aplikaci Warehouse Mobile App (WMA) při zahájení práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="8e47c-311">Vyberte <strong>Navrhnout</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="8e47c-312">Potvrďte nové skladové místo navrhované na základě dostupnosti množství dávky.</span><span class="sxs-lookup"><span data-stu-id="8e47c-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-313">Při aktuální práci dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="8e47c-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="8e47c-314">Místo na řádku výdeje je aktualizováno na nové místo.</span><span class="sxs-lookup"><span data-stu-id="8e47c-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="8e47c-315">(Je-li toto umístění řízeno registrační značkou, je k skladové transakci práce přiřazena náhodná registrační značka a pracovník může vybírat z registračních značek, které mají dostupné množství.)</span><span class="sxs-lookup"><span data-stu-id="8e47c-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="8e47c-316">Pokud se množství nachází na více než jedné registrační značce v novém skladovém místě, bude původní řádek výdeje rozdělen do několika řádků tak, aby souhlasila každá registrační značka.</span><span class="sxs-lookup"><span data-stu-id="8e47c-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-317">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-318">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-319">Vyberte položku nabídky <strong>Přepsat umístění</strong> ve WMA při zahájení práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="8e47c-320">Zadat ručně místo.</span><span class="sxs-lookup"><span data-stu-id="8e47c-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-321">Akce <strong>Přepsání místa</strong> není možná.</span><span class="sxs-lookup"><span data-stu-id="8e47c-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="8e47c-322">Dojde k selhání a dojde k vyvolání chyby.</span><span class="sxs-lookup"><span data-stu-id="8e47c-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="8e47c-323">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="8e47c-324">Tlačítko Úplné – rozdělení řádku práce z důvodu přetečení v umístění uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-325">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-326">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-327">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-327">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-328">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-328">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-329">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e47c-330">Možnost <strong>Povolit rozdělení práce</strong> je povolena na položce nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="8e47c-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="8e47c-331">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-332">Vyberte položku nabídky <strong>Úplný</strong> ve WMA při zpracování práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="8e47c-333">Do pole <strong>Vyskladněné množství</strong> zadejte částečné množství požadovaného výdeje, které označuje plnou kapacitu.</span><span class="sxs-lookup"><span data-stu-id="8e47c-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="8e47c-334">Při aktuální práci je množství aktualizováno na zbývající množství, které musí být vyskladněno.</span><span class="sxs-lookup"><span data-stu-id="8e47c-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="8e47c-335">Nová práce pro vyskladněné množství je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="8e47c-336">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="8e47c-337">Snížení vyskladněného množství dokončené práce (z nákladu)</span><span class="sxs-lookup"><span data-stu-id="8e47c-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-338">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-339">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-340">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-340">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-341">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-341">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-342">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-343">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-343">Not applicable</span></span></td>
<td><span data-ttu-id="8e47c-344">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-345">Otevřete stránku <strong>Snížit vyskladněné množství</strong> z řádku vytížení.</span><span class="sxs-lookup"><span data-stu-id="8e47c-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="8e47c-346">Zadejte úplné množství pro zrušení výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="8e47c-347">Vyberte přesun do místa / na registrační značku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="8e47c-348">Práce, která je přidružená k řádku vytížení, je zrušena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="8e47c-349">Nová práce pro přesun zásob je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-350">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-351">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-352">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-352">No</span></span></td>
<td><span data-ttu-id="8e47c-353">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-353">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-354">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-354">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-355">Množství je znovu rezervováno pro stejnou dávku a pro stejné skladové místo a registrační značku (jedná-li se o místo řízené registrační značkou), které byly zadány při zrušení výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="8e47c-356">Přesunutí položky v rámci skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="8e47c-357">Tuto akci skladu lze použít pouze pro přesun typu **Proces pro vytvoření práce**, nikoli pro přesun podle šablony.</span><span class="sxs-lookup"><span data-stu-id="8e47c-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-358">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-359">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-360">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-360">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-361">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-361">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-362">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-363">Možnost <strong>Povolit pohyb zásob s přidruženou prací</strong> je povolena u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8e47c-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="8e47c-364">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-365">Zahajte přesun ve WMA.</span><span class="sxs-lookup"><span data-stu-id="8e47c-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="8e47c-366">Zadejte místa z a do.</span><span class="sxs-lookup"><span data-stu-id="8e47c-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="8e47c-367">Ve všech existujících pracích, které jsou přesunutím ovlivněny, se skladové místo výdeje aktualizuje na nové umístění "do".</span><span class="sxs-lookup"><span data-stu-id="8e47c-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="8e47c-368">Nová práce pro přesun zásob je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-369">Všechny stávající rezervace, které jsou ovlivněny pohybem množství z daného skladového místa, budou znovu rezervovány pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-370">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-371">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-371">No</span></span></td>
<td><span data-ttu-id="8e47c-372">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-372">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-373">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-373">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-374">Všechny stávající rezervace, které jsou ovlivněny pohybem množství z daného skladového místa, jsou znovu rezervovány pro stejnou dávku a pro nové umístění "do" a registrační značku (pokud je toto umístění řízeno registrační značkou).</span><span class="sxs-lookup"><span data-stu-id="8e47c-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="8e47c-375">Rezervace vyskladněného množství dokončené práce (z nákladu nebo vlny)</span><span class="sxs-lookup"><span data-stu-id="8e47c-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-376">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-377">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-378">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-378">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-379">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-379">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-380">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="8e47c-381">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-381">Not applicable</span></span></td>
<td><span data-ttu-id="8e47c-382">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-383">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="8e47c-384">Na stránce s požadavkem vyberte možnost <strong>Ponechat položky v aktuálním umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-385">Veškerá práce, která je přidružená k řádku vytížení, je zrušena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="8e47c-386">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-387">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-388">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-388">No</span></span></td>
<td><span data-ttu-id="8e47c-389">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-389">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-390">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-390">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-391">Množství je znovu rezervováno pro stejnou dávku a pro místo a registrační značku, kde bylo množství ponecháno při stornování.</span><span class="sxs-lookup"><span data-stu-id="8e47c-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-392">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-393">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="8e47c-394">Na stránce s požadavkem vyberte možnost <strong>Přiřadit položky k tomuto umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="8e47c-395">Aktuální práce je zrušena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="8e47c-396">Nová práce pro přesun zásob je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="8e47c-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-397">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-398">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-399">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-399">No</span></span></td>
<td><span data-ttu-id="8e47c-400">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-400">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-401">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-401">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-402">Množství je znovu rezervováno pro stejnou dávku a pro místo a registrační značku, kterým bylo množství přiřazeno při stornování.</span><span class="sxs-lookup"><span data-stu-id="8e47c-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-403">Ano/Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-404">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="8e47c-405">Na stránce s požadavkem vyberte možnost <strong>Přesunout položky do tohoto umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-406">Storno není podporováno.</span><span class="sxs-lookup"><span data-stu-id="8e47c-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="8e47c-407">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-408">Ano/Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-409">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="8e47c-410">Na stránce s požadavkem vyberte možnost <strong>Přesunout položky podle směrnic skladového umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-411">Storno není podporováno.</span><span class="sxs-lookup"><span data-stu-id="8e47c-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="8e47c-412">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="8e47c-413">Krátkodobý výdej a množství – Zaregistrujte množství jako fyzicky nenalezené nav místě nebo na registrační značce během provádění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-414">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-415">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-416">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-416">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-417">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-417">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-418">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-419">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Žádný</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="8e47c-420">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-421">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> ve WMA při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="8e47c-422">Do pole <strong>Vyskladněné množství</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="8e47c-423">Do pole <strong>Důvod</strong> zadejte <strong>Žádné opakované přidělení</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="8e47c-424">Aktuální práce je uzavřena a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="8e47c-425">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="8e47c-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-426">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-427">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-428">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-428">No</span></span></td>
<td><span data-ttu-id="8e47c-429">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="8e47c-430">Akce krátkodobého výdeje se nezdaří a dojde k vyvolání chyby.</span><span class="sxs-lookup"><span data-stu-id="8e47c-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="8e47c-431">Aktuální práce zůstane otevřená.</span><span class="sxs-lookup"><span data-stu-id="8e47c-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-432">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-433">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Žádný</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="8e47c-434">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-435">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> ve WMA při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="8e47c-436">Do pole <strong>Vyskladněné množství</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="8e47c-437">Do pole <strong>Důvod</strong> zadejte <strong>Žádné opakované přidělení</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="8e47c-438">Aktuální práce je uzavřena a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="8e47c-439">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="8e47c-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-440">Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě krátkodobého výdeje, budou znovu rezervovány pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-441">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-442">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-442">No</span></span></td>
<td><span data-ttu-id="8e47c-443">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-443">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-444">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-444">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-445">Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě krátkodobého výdeje, budou odstraněny.</span><span class="sxs-lookup"><span data-stu-id="8e47c-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-446">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne/Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="8e47c-447">Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8e47c-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="8e47c-448">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-449">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> ve WMA při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="8e47c-450">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="8e47c-451">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="8e47c-452">V seznamu vyberte umístění/registrační značku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="8e47c-453">Při aktuální práci dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="8e47c-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="8e47c-454">Řádek výdeje je uzavřen a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="8e47c-455">Řádek vložení je zrušen.</span><span class="sxs-lookup"><span data-stu-id="8e47c-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="8e47c-456">Je vytvořen nový řádek vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="8e47c-456">A new pick line is created.</span></span> <span data-ttu-id="8e47c-457">Používá se místo / registrační značka, které uživatel vybral.</span><span class="sxs-lookup"><span data-stu-id="8e47c-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="8e47c-458">Je vytvořen nový řádek vložení.</span><span class="sxs-lookup"><span data-stu-id="8e47c-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8e47c-459">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="8e47c-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-460">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-461">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="8e47c-462">Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8e47c-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="8e47c-463">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-464">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> ve WMA při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="8e47c-465">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="8e47c-466">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-467">Akce krátkodobého výdeje se nezdaří a dojde k vyvolání chyby.</span><span class="sxs-lookup"><span data-stu-id="8e47c-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="8e47c-468">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-469">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="8e47c-470">Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8e47c-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="8e47c-471">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-472">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> ve WMA při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="8e47c-473">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="8e47c-474">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="8e47c-475">V seznamu vyberte umístění/registrační značku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="8e47c-476">Při aktuální práci dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="8e47c-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="8e47c-477">Řádek výdeje je uzavřen a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="8e47c-478">Řádek vložení je zrušen.</span><span class="sxs-lookup"><span data-stu-id="8e47c-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8e47c-479">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="8e47c-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="8e47c-480">Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě /registrační značce krátkodobého výdeje, budou odstraněny.</span><span class="sxs-lookup"><span data-stu-id="8e47c-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-481">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Automatický</strong>, <strong>Úprava zásob</strong> = <strong>Ano/Ne</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano/Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="8e47c-482">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="8e47c-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-483">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> ve WMA při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="8e47c-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="8e47c-484">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="8e47c-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="8e47c-485">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s automaticky opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-486">Krátkodobé výdeje, které zahrnují automatické opětovné přidělení, nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="8e47c-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="8e47c-487">Krátkodobé výdeje, které zahrnují automatické opětovné přidělení, nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="8e47c-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="8e47c-488">Změnit stav zásob</span><span class="sxs-lookup"><span data-stu-id="8e47c-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="8e47c-489">Tuto akci skladu lze provést z více vstupních bodů.</span><span class="sxs-lookup"><span data-stu-id="8e47c-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="8e47c-490">Zde zobrazený příklad používá akci **Změna stavu zásob** na stránce **Množství na skladě podle místa**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8e47c-491">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="8e47c-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="8e47c-492">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="8e47c-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="8e47c-493">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="8e47c-493">Key user steps</span></span></th>
<th><span data-ttu-id="8e47c-494">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="8e47c-494">Warehouse work</span></span></th>
<th><span data-ttu-id="8e47c-495">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="8e47c-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-496">Na kartě <strong>Sklad</strong> v záznamu <strong>Sklad</strong> je pole <strong>Odstranit rezervace a označení</strong> nastaveno na <strong>Rezervace</strong> nebo <strong>Označení a rezervace</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="8e47c-497">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-498">Vyberte konkrétní umístění.</span><span class="sxs-lookup"><span data-stu-id="8e47c-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="8e47c-499">Vyberte řádek s určitou položkou, skladovým místem a registrační značkou (je-li toto umístění řízeno registrační značkou).</span><span class="sxs-lookup"><span data-stu-id="8e47c-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="8e47c-500">Zvolte <strong>Změna stavu zásob</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="8e47c-501">Nastavte pole <strong>Stav zásob</strong> na <strong>Blokování</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-502">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="8e47c-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="8e47c-503">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-504">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="8e47c-505">Jsou vytvořeny dvě skladové transakce typu <strong>Změna stavu zásob</strong>, které reprezentují změnu v dimenzi stavu zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="8e47c-506">Vytvoří se skladová transakce typu <strong>Blokování zásob</strong> a typu výdeje <strong>Rezervované – fyzicky</strong>, která představuje rezervaci blokovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8e47c-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-507">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-507">No</span></span></td>
<td><span data-ttu-id="8e47c-508">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-508">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-509">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="8e47c-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="8e47c-510">Rezervace je odebrána.</span><span class="sxs-lookup"><span data-stu-id="8e47c-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="8e47c-511">Jsou vytvořeny dvě skladové transakce typu <strong>Změna stavu zásob</strong>, které reprezentují změnu v dimenzi stavu zásob.</span><span class="sxs-lookup"><span data-stu-id="8e47c-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="8e47c-512">Vytvoří se skladová transakce typu <strong>Blokování zásob</strong> a typu výdeje <strong>Rezervované – fyzicky</strong>, která představuje rezervaci blokovaného množství.</span><span class="sxs-lookup"><span data-stu-id="8e47c-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="8e47c-513">Na kartě <strong>Sklad</strong> v záznamu <strong>Sklad</strong> je pole <strong>Odstranit rezervace a označení</strong> nastaveno na <strong>Žádná</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="8e47c-514">Ano</span><span class="sxs-lookup"><span data-stu-id="8e47c-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="8e47c-515">Vyberte konkrétní umístění.</span><span class="sxs-lookup"><span data-stu-id="8e47c-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="8e47c-516">Vyberte řádek s určitou položkou, skladovým místem a registrační značkou (je-li toto umístění řízeno registrační značkou).</span><span class="sxs-lookup"><span data-stu-id="8e47c-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="8e47c-517">Zvolte <strong>Změna stavu zásob</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="8e47c-518">Nastavte pole <strong>Stav zásob</strong> na <strong>Blokování</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e47c-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="8e47c-519">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="8e47c-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="8e47c-520">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="8e47c-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="8e47c-521">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8e47c-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e47c-522">Ne</span><span class="sxs-lookup"><span data-stu-id="8e47c-522">No</span></span></td>
<td><span data-ttu-id="8e47c-523">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="8e47c-523">See the previous row.</span></span></td>
<td><span data-ttu-id="8e47c-524">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="8e47c-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="8e47c-525">Změny stavu zásob nejsou povoleny.</span><span class="sxs-lookup"><span data-stu-id="8e47c-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="8e47c-526">Omezení</span><span class="sxs-lookup"><span data-stu-id="8e47c-526">Limitations</span></span>

- <span data-ttu-id="8e47c-527">Flexibilní funkce rezervace dimenzí na úrovni skladu nepodporuje následující funkce:</span><span class="sxs-lookup"><span data-stu-id="8e47c-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="8e47c-528">Správa skutečné hmotnosti</span><span class="sxs-lookup"><span data-stu-id="8e47c-528">Catch weight management</span></span>
    - <span data-ttu-id="8e47c-529">Záporný fyzický sklad</span><span class="sxs-lookup"><span data-stu-id="8e47c-529">Physical negative inventory</span></span>
    - <span data-ttu-id="8e47c-530">Rezervace proti objednané dodávce</span><span class="sxs-lookup"><span data-stu-id="8e47c-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="8e47c-531">Převodní příkazy a výdej surovin</span><span class="sxs-lookup"><span data-stu-id="8e47c-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="8e47c-532">Pravidlo konsolidace kontejneru pro balení podle jednotky předpisu má omezení.</span><span class="sxs-lookup"><span data-stu-id="8e47c-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="8e47c-533">V případě rezervací potvrzených objednávkou doporučujeme nepoužívat šablony sestavení kontejnerů, kde je povoleno pole **Zabalit podle jednotky přepisu**.</span><span class="sxs-lookup"><span data-stu-id="8e47c-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="8e47c-534">V aktuálním návrhu nejsou při vytvoření skladové práce použity směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8e47c-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="8e47c-535">Z tohoto důvodu je při kroku vlny vytváření kontejnerů použita pouze nejnižší jednotka ve skupině klasifikace jednotek (skladová jednotka).</span><span class="sxs-lookup"><span data-stu-id="8e47c-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
