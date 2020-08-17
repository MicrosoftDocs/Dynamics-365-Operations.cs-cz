---
title: Flexibilní zásada rezervace dimenze na úrovni skladu
description: V tomto tématu jsou popsány zásady rezervace zásob, které umožňují společnostem prodávat produkty sledované podle dávky a spustit jejich logistiku, protože operace s povoleným WMS rezervují konkrétní dávky pro prodejní objednávky zákazníka, a to i v případě, že hierarchie rezervací, přidružená k produktům, neumožňuje rezervaci specifických dávek.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 65304216b579b8def493d1e4218174cb9617013d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652172"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="33871-103">Flexibilní zásada rezervace dimenze na úrovni skladu</span><span class="sxs-lookup"><span data-stu-id="33871-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33871-104">Pokud je hierarchie rezervací zásob typu Batch-below\[location\] spojena s produkty, podniky, které prodávají produkty sledované podle dávky a spouštějí své logistiku jako operace, které jsou povoleny pro Microsoft Dynamics 365 Warehouse Management System (WMS), nemohou rezervovat konkrétní dávky těchto produktů pro prodejní objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="33871-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="33871-105">Podobně nemohou být vyhrazeny konkrétní registrační značky pro produkty na prodejních objednávkách, pokud jsou tyto produkty spojeny s výchozí hierarchií rezervace.</span><span class="sxs-lookup"><span data-stu-id="33871-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="33871-106">V tomto tématu jsou popsány zásady rezervace zásob, které těmto podnikům umožňují rezervovat specifické dávky nebo registrační značky, a to i v případě, že jsou produkty přiřazeny k hierarchii rezervací Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="33871-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="33871-107">Hierarchie rezervací zásob</span><span class="sxs-lookup"><span data-stu-id="33871-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="33871-108">V tomto oddílu je shrnuta existující hierarchie rezervací zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="33871-109">Hierarchie rezervace zásob určuje, že pokud se jedná o dimenze uskladnění, objednávka poptávky nese povinné dimenze pracoviště, skladu a stavu zásob, zatímco logika skladu je odpovědná za přiřazení skladového místa k požadovanému množství a rezervaci skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="33871-110">Jinak řečeno, v interakcích mezi objednávkou poptávky a skladovými operacemi se očekává, že objednávka poptávky indikuje, odkud musí být objednávka expedována (tj. pracoviště a sklad).</span><span class="sxs-lookup"><span data-stu-id="33871-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="33871-111">Sklad pak spoléhá na svou logiku k nalezení požadovaného množství v skladových prostorách.</span><span class="sxs-lookup"><span data-stu-id="33871-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="33871-112">Chcete-li však zohlednit provozní model podniku, je sledovací dimenze (dávka a sériová čísla) předmětem větší flexibility.</span><span class="sxs-lookup"><span data-stu-id="33871-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="33871-113">Hierarchie rezervací zásob může vyhovovat situacím, pro které platí následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="33871-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="33871-114">Podnik spoléhá na své skladové operace za účelem správy výdeje množství, která mají čísla dávek nebo sériová čísla po nalezení množství v prostoru úložiště skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="33871-115">Tento model se často označuje jako *Batch-below\[location\]*.</span><span class="sxs-lookup"><span data-stu-id="33871-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="33871-116">Obvykle se používá v případě, že identifikace dávky nebo sériového čísla produktu není důležitá pro zákazníky, kteří učiní poptávku u prodávající společnosti.</span><span class="sxs-lookup"><span data-stu-id="33871-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="33871-117">Pokud jsou dávka a sériová čísla součástí specifikace objednávky odběratele a jsou zaznamenána na objednávce poptávky, skladové operace, které vyhledají množství ve skladu, jsou omezeny konkrétními požadovanými počty a nejsou povoleny jejich změny.</span><span class="sxs-lookup"><span data-stu-id="33871-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="33871-118">Tento model se označuje jako *Batch-above\[location\]*.</span><span class="sxs-lookup"><span data-stu-id="33871-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="33871-119">V těchto scénářích je výzvou, že každému uvolněnému produktu lze přiřadit pouze jednu hierarchii rezervace zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="33871-120">Proto, aby WMS zpracoval sledované položky, poté, co v přiřazení hierarchie určí, kdy má být provedena rezervace dávky nebo sériového čísla (buď při objednávce poptávky nebo při zahájení práce výdeje skladu), toto časování nelze změnit ad hoc.</span><span class="sxs-lookup"><span data-stu-id="33871-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="33871-121">Pružná rezervace pro položky sledované dávkou</span><span class="sxs-lookup"><span data-stu-id="33871-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="33871-122">Scénáře obchodu</span><span class="sxs-lookup"><span data-stu-id="33871-122">Business scenario</span></span>

<span data-ttu-id="33871-123">V tomto scénáři společnost používá strategii zásob, při které je dokončené zboží sledováno pomocí čísel dávek.</span><span class="sxs-lookup"><span data-stu-id="33871-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="33871-124">Tato společnost také používá pracovní vytížení WMS.</span><span class="sxs-lookup"><span data-stu-id="33871-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="33871-125">Vzhledem k tomu, že toto pracovní vytížení má dobře vybavenou logiku pro plánování a provádění operací výdeje a expedice skladu pro položky s povolenou dávkou, je většina dokončených položek přidružena k hierarchii rezervací zásob "Batch-below\[location\]".</span><span class="sxs-lookup"><span data-stu-id="33871-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="33871-126">Výhodou tohoto typu operačního nastavení je to, že rozhodnutí (což jsou ve skutečnosti rozhodnutí o rezervacích) o tom, které dávky vyskladnit a do jakého skladu je vložit, budou odloženy až do zahájení operace výdeje skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="33871-127">Nejsou provedeny při učinění objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="33871-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="33871-128">Ačkoliv hierarchie rezervací Batch-below\[location\] slouží k zajištění správných obchodních cílů společnosti, mnoho zavedených zákazníků společnosti vyžaduje stejnou dávku, při které byly tyto produkty zakoupeny dříve.</span><span class="sxs-lookup"><span data-stu-id="33871-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="33871-129">Z toho vyplývá, že společnost hledá flexibilitu ve způsobu, jakým jsou zpracovávána pravidla rezervace dávky, takže v závislosti na poptávce odběratelů po stejné položce dojde k následujícímu chování:</span><span class="sxs-lookup"><span data-stu-id="33871-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="33871-130">Číslo dávky lze zaznamenat a rezervovat, když je objednávka provedena, zpracovatelem prodeje, a nelze ji změnit během skladových operací anebo pořídit jinými požadavky.</span><span class="sxs-lookup"><span data-stu-id="33871-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="33871-131">Toto chování pomáhá zaručit, že objednané číslo dávky je expedováno odběrateli.</span><span class="sxs-lookup"><span data-stu-id="33871-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="33871-132">Není-li číslo dávky pro odběratele důležité, skladové operace mohou určit číslo dávky během výdejní práce po provedení registrace prodejní objednávky a rezervace.</span><span class="sxs-lookup"><span data-stu-id="33871-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="33871-133">Povolení rezervace konkrétní dávky v prodejní objednávce</span><span class="sxs-lookup"><span data-stu-id="33871-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="33871-134">Chcete-li přizpůsobit požadovanou flexibilitu v chování rezervace dávek u položek, které jsou přidruženy k hierarchii rezervace zásob Batch-below\[location\], musí manažeři zásob zaškrtnout políčko **Povolit rezervaci na objednávce poptávky** pro úroveň **čísla dávky** na stránce **hierarchie rezervací zásob**.</span><span class="sxs-lookup"><span data-stu-id="33871-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Zflexibilnění hierarchie rezervace zásob](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="33871-136">Je- li vybrána úroveň **čísla dávky** v hierarchii, budou automaticky vybrány všechny dimenze nad úrovní a až k úrovni **skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="33871-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="33871-137">(Ve výchozím nastavení jsou přednastaveny všechny dimenze nad úrovní **skladového místa**.) Toto chování odpovídá logice, kde jsou všechny dimenze v rozsahu mezi číslem dávky a místem automaticky rezervovány po rezervaci konkrétního čísla dávky na řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="33871-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="33871-138">Zaškrtávací políčko **Povolit rezervaci na objednávce poptávky** se vztahuje pouze na úrovně hierarchie rezervací, které jsou pod dimenzí skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="33871-139">**Číslo dávky** a **Registrační značka** je jediná úroveň v hierarchii, která je otevřená pro zásadu pružné rezervace.</span><span class="sxs-lookup"><span data-stu-id="33871-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="33871-140">Jinými slovy, pro úroveň **umístění** nebo **sériového čísla** nelze zaškrtnout políčko **Povolit rezervaci na objednávce poptávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="33871-141">Pokud hierarchie rezervace obsahuje dimenzi sériového čísla (která musí vždy být nižší než úroveň **Číslo dávky**) a pokud jste pro číslo dávky aktivovali rezervaci specifickou pro dávku, systém bude pokračovat ve zpracování rezervací sériových čísel a operací výdeje na základě pravidel, která platí pro zásadu rezervace Serial-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="33871-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="33871-142">V kterémkoli bodě můžete povolit rezervaci specifickou pro dávku pro existující hierarchii rezervací Batch-below\[location\] v rámci vašeho nasazení.</span><span class="sxs-lookup"><span data-stu-id="33871-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="33871-143">Tato změna neovlivní žádné rezervace a otevřené práce skladu, které byly vytvořeny před provedením změny.</span><span class="sxs-lookup"><span data-stu-id="33871-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="33871-144">Zaškrtnutí políčka **Povolit rezervaci na objednávce poptávky** však nelze odstranit, pokud pro jednu nebo více položek které jsou přidruženy k dané hierarchii rezervací, existují transakce zásob typů výdeje **Rezervované objednané**, **Rezervované – fyzicky**, nebo **Objednáno**.</span><span class="sxs-lookup"><span data-stu-id="33871-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="33871-145">Pokud existující hierarchie rezervací položky nepovoluje dávkovou specifikaci pro objednávku, můžete ji přiřadit k hierarchii rezervací, která povoluje specifikaci dávky, pokud je struktura úrovně hierarchie v obou hierarchiích stejná.</span><span class="sxs-lookup"><span data-stu-id="33871-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="33871-146">Použijte funkci **Změnit hierarchii rezervací pro položky** pro provedení opětovného přiřazení.</span><span class="sxs-lookup"><span data-stu-id="33871-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="33871-147">Tato změna může být důležitá v případě, že chcete zabránit flexibilní rezervaci dávky pro podmnožinu položek sledovaných dávkou, ale povolit ji pro zbytek portfolia produktů.</span><span class="sxs-lookup"><span data-stu-id="33871-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="33871-148">Bez ohledu na to, zda jste zaškrtli políčko **Povolit rezervaci na objednávce poptávky**, nechcete-li rezervovat určité číslo dávky pro položku na řádku objednávky, bude stále platit výchozí logika skladového místa, která je platná pro hierarchii rezervace Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="33871-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="33871-149">Rezervace konkrétního čísla dávky pro objednávku odběratele</span><span class="sxs-lookup"><span data-stu-id="33871-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="33871-150">Po nastavení hierarchie rezervací zásob Batch-below\[location\] pro položku sledovanou dávkou za účelem umožnění rezervace konkrétních čísel dávky na prodejních objednávkách mohou zpracovatelé prodejní objednávky provést objednávky odběratele pro stejnou položku jedním z následujících způsobů:</span><span class="sxs-lookup"><span data-stu-id="33871-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="33871-151">**Zadat podrobnosti objednávky bez zadání čísla dávky** – tento přístup by měl být použit v případě, že specifikace dávky produktu není pro odběratele důležitá.</span><span class="sxs-lookup"><span data-stu-id="33871-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="33871-152">Všechny existující procesy související se zpracováním objednávky tohoto typu v systému zůstanou nezměněny.</span><span class="sxs-lookup"><span data-stu-id="33871-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="33871-153">Na straně uživatelů nejsou vyžadovány žádné další úvahy.</span><span class="sxs-lookup"><span data-stu-id="33871-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="33871-154">**Zadat podrobnosti objednávky a rezervovat určité číslo dávky** – tento přístup by měl být použit v případě, že odběratel požaduje určitou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="33871-155">Zákazníci obvykle požadují určitou dávku při opětovném objednání produktu, který dříve nakoupili.</span><span class="sxs-lookup"><span data-stu-id="33871-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="33871-156">Tento typ rezervace specifické pro dávku se nazývá *rezervace potvrzená objednávkou*.</span><span class="sxs-lookup"><span data-stu-id="33871-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="33871-157">Následující sada pravidel je platná při zpracování množství a číslo dávky je potvrzeno pro specifickou objednávku:</span><span class="sxs-lookup"><span data-stu-id="33871-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="33871-158">Chcete-li povolit rezervaci určitého čísla dávky pro položku pod zásadami rezervace Batch-below\[location\], musí systém rezervovat všechny dimenze v rámci skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="33871-159">Tento rozsah obvykle zahrnuje dimenzi registrační značky.</span><span class="sxs-lookup"><span data-stu-id="33871-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="33871-160">Směrnice skladových míst se nepoužívají, pokud je pro řádek prodeje vytvořena výdejní práce, která používá rezervaci dávky potvrzenou objednávkou.</span><span class="sxs-lookup"><span data-stu-id="33871-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="33871-161">Během zpracování práce skladu pro dávky potvrzené objednávkou nemůže uživatel ani systém změnit číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="33871-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="33871-162">(Toto zpracování zahrnuje zpracování výjimek.)</span><span class="sxs-lookup"><span data-stu-id="33871-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="33871-163">Následující příklad ukazuje celý tok.</span><span class="sxs-lookup"><span data-stu-id="33871-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="33871-164">Příklad scénáře: Přidělení čísla dávky</span><span class="sxs-lookup"><span data-stu-id="33871-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="33871-165">Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="33871-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="33871-166">Nastavení hierarchie rezervací zásob, aby byla povolena rezervace specifická pro dávku</span><span class="sxs-lookup"><span data-stu-id="33871-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="33871-167">Přejděte na **Řízení skladu** \> **Nastavení** \> **Zásoby \> Hierarchie rezervací**.</span><span class="sxs-lookup"><span data-stu-id="33871-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="33871-168">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="33871-168">Select **New**.</span></span>
3. <span data-ttu-id="33871-169">Do pole **Název** zadejte název (například **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="33871-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="33871-170">Do pole **Popis** zadejte popis (například **Batch below flexible**).</span><span class="sxs-lookup"><span data-stu-id="33871-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="33871-171">V poli **Vybrané** zvolte **Sériové číslo** a **Vlastník** a poté zvolte tlačítko šipky doleva pro přesun na pole **K dipozici**.</span><span class="sxs-lookup"><span data-stu-id="33871-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="33871-172">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="33871-172">Select **OK**.</span></span>
7. <span data-ttu-id="33871-173">V řádku pro úroveň dimenze **Číslo dávky** zaškrtněte políčko **Povolit rezervaci na objednávce poptávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="33871-174">Úrovně **Registrační značka** a **Skladové místo** jsou vybrány automaticky a nelze u nich zrušit zaškrtávací políčko.</span><span class="sxs-lookup"><span data-stu-id="33871-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="33871-175">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="33871-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="33871-176">Vytvoření nového uvolněného produktu</span><span class="sxs-lookup"><span data-stu-id="33871-176">Create a new released product</span></span>

1. <span data-ttu-id="33871-177">Pomocí těchto hodnot nastavíte tři základní datové parametry produktu:</span><span class="sxs-lookup"><span data-stu-id="33871-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="33871-178">V poli **Skupina dimenze úložiště** vyberte **Ware**.</span><span class="sxs-lookup"><span data-stu-id="33871-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="33871-179">V poli **Skupina sledovací dimenze** vyberte **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="33871-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="33871-180">V poli **Hierarchie rezervace** vyberte **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="33871-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="33871-181">Vytvořte dvě čísla dávek, jako například **B11** a **B22**.</span><span class="sxs-lookup"><span data-stu-id="33871-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="33871-182">Přidejte množství položek k zásobám na skladě pomocí následujících hodnot.</span><span class="sxs-lookup"><span data-stu-id="33871-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="33871-183">Sklad</span><span class="sxs-lookup"><span data-stu-id="33871-183">Warehouse</span></span> | <span data-ttu-id="33871-184">Číslo dávky</span><span class="sxs-lookup"><span data-stu-id="33871-184">Batch number</span></span> | <span data-ttu-id="33871-185">Umístění</span><span class="sxs-lookup"><span data-stu-id="33871-185">Location</span></span> | <span data-ttu-id="33871-186">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="33871-186">License plate</span></span> | <span data-ttu-id="33871-187">Množství</span><span class="sxs-lookup"><span data-stu-id="33871-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="33871-188">24</span><span class="sxs-lookup"><span data-stu-id="33871-188">24</span></span>        | <span data-ttu-id="33871-189">B11</span><span class="sxs-lookup"><span data-stu-id="33871-189">B11</span></span>          | <span data-ttu-id="33871-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="33871-190">BULK-001</span></span> | <span data-ttu-id="33871-191">Žádní</span><span class="sxs-lookup"><span data-stu-id="33871-191">None</span></span>          | <span data-ttu-id="33871-192">10</span><span class="sxs-lookup"><span data-stu-id="33871-192">10</span></span>       |
    | <span data-ttu-id="33871-193">24</span><span class="sxs-lookup"><span data-stu-id="33871-193">24</span></span>        | <span data-ttu-id="33871-194">B11</span><span class="sxs-lookup"><span data-stu-id="33871-194">B11</span></span>          | <span data-ttu-id="33871-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="33871-195">FL-001</span></span>   | <span data-ttu-id="33871-196">LP11</span><span class="sxs-lookup"><span data-stu-id="33871-196">LP11</span></span>          | <span data-ttu-id="33871-197">10</span><span class="sxs-lookup"><span data-stu-id="33871-197">10</span></span>       |
    | <span data-ttu-id="33871-198">24</span><span class="sxs-lookup"><span data-stu-id="33871-198">24</span></span>        | <span data-ttu-id="33871-199">B22</span><span class="sxs-lookup"><span data-stu-id="33871-199">B22</span></span>          | <span data-ttu-id="33871-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="33871-200">FL-002</span></span>   | <span data-ttu-id="33871-201">LP22</span><span class="sxs-lookup"><span data-stu-id="33871-201">LP22</span></span>          | <span data-ttu-id="33871-202">10</span><span class="sxs-lookup"><span data-stu-id="33871-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="33871-203">Zadání podrobností prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="33871-203">Enter sales order details</span></span>

1. <span data-ttu-id="33871-204">Přejděte na **Prodej a marketing** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="33871-205">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="33871-205">Select **New**.</span></span>
3. <span data-ttu-id="33871-206">V záhlaví prodejní objednávky v poli **Účet odběratele** zadejte **US-003**.</span><span class="sxs-lookup"><span data-stu-id="33871-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="33871-207">Přidejte řádek pro novou položku a jako množství zadejte **10**.</span><span class="sxs-lookup"><span data-stu-id="33871-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="33871-208">Ujistěte se, že je v poli **Sklad** nastavena hodnota na **24**.</span><span class="sxs-lookup"><span data-stu-id="33871-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="33871-209">Na záložce s náhledem **Řádky prodejní objednávky** vyberte možnost **Zásoby** a poté ve skupině **Udržovat** vyberte možnost **Rezervace dávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="33871-210">Stránka **Rezervace dávky** zobrazí seznam dávek, které jsou k dispozici pro rezervaci pro daný řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="33871-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="33871-211">V tomto příkladu se zobrazí množství **20** pro číslo dávky **B11** a množství **10** pro číslo dávky **B22**.</span><span class="sxs-lookup"><span data-stu-id="33871-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="33871-212">Všimněte si, ke stránce **Rezervace dávky** nelze získat přístup z řádku, pokud je položka na tomto řádku přidružena k hierarchii rezervace Batch-below\[location\] v případě, že není nastavena tak, aby umožňovala rezervaci specifickou pro dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33871-213">Chcete-li rezervovat určitou dávku pro prodejní objednávku, je nutné použít stránku **Rezervace dávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="33871-214">Zadáte-li číslo dávky přímo do řádku prodejní objednávky, systém se bude chovat, jako byste zadali konkrétní hodnotu dávky pro položku, na kterou se vztahuje zásada rezervace Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="33871-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="33871-215">Po uložení řádku se zobrazí varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="33871-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="33871-216">Pokud potvrdíte, že číslo dávky by mělo být zadáno přímo na řádku objednávky, řádek nebude zpracován běžnou logikou správy skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="33871-217">Pokud rezervujete množství na stránce **Rezervace**, žádná specifická dávka nebude rezervována a provedení skladových operací pro tento řádek bude následovat pravidla aplikovatelná pod zásadami rezervace Batch-below\[location\].</span><span class="sxs-lookup"><span data-stu-id="33871-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="33871-218">Tato stránka obecně funguje a je v interakci stejným způsobem, jako pracuje a je závislá na položkách, které mají přidruženou hierarchii rezervací typu Batch-above\[location\].</span><span class="sxs-lookup"><span data-stu-id="33871-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="33871-219">Platí však následující výjimky:</span><span class="sxs-lookup"><span data-stu-id="33871-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="33871-220">Záložka s náhledem **Čísla dávek potvrzená pro řádek zdroje** zobrazí čísla dávek, která jsou vyhrazena pro řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="33871-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="33871-221">Hodnoty dávky v mřížce se zobrazí v průběhu cyklu realizace řádku objednávky včetně fází zpracování skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="33871-222">Naopak na záložce s náhledem **Přehled** je běžná rezervace řádku objednávky (tj. rezervace, která se provádí pro dimenze nad úrovní **skladového místa**), v mřížce zobrazena až do bodu vytvoření skladové práce.</span><span class="sxs-lookup"><span data-stu-id="33871-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="33871-223">Entita práce pak převezme rezervaci řádku a na stránce se již nebude zobrazovat rezervace řádku.</span><span class="sxs-lookup"><span data-stu-id="33871-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="33871-224">Záložka s náhledem **Čísla dávek potvrzená pro řádek zdroje** pomáhá zajistit, že procesor prodejní objednávky může zobrazit čísla dávek, která byla potvrzena do objednávky zákazníka v kterémkoli okamžiku během svého životního cyklu, až do fakturace.</span><span class="sxs-lookup"><span data-stu-id="33871-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="33871-225">Kromě rezervace konkrétní dávky může uživatel ručně vybrat konkrétní místo dávky a registrační značku namísto toho, aby je systém vybral automaticky.</span><span class="sxs-lookup"><span data-stu-id="33871-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="33871-226">Tato schopnost souvisí s návrhem mechanismu rezervace dávky potvrzené objednávkou.</span><span class="sxs-lookup"><span data-stu-id="33871-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="33871-227">Jak bylo zmíněno dříve, chcete-li povolit rezervaci určitého čísla dávky pro položku pod zásadami rezervace Batch-below\[location\], musí systém rezervovat všechny dimenze v rámci skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="33871-228">Skladová práce proto bude mít stejné dimenze uskladnění, které byly rezervovány uživateli, kteří pracovali s objednávkami, a nemusí vždy představovat umístění úložiště položek, které je pro operace výdeje vhodné nebo dokonce možné.</span><span class="sxs-lookup"><span data-stu-id="33871-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="33871-229">Pokud zpracovatelé objednávek vědí o omezeních skladu, mohou chtít ručně vybrat určitá skladová místa a registrační značky při rezervaci dávky.</span><span class="sxs-lookup"><span data-stu-id="33871-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="33871-230">V takovém případě musí uživatel použít funkci **Zobrazit dimenze** v záhlaví stránky a přidat umístění a registrační značku do mřížky na záložce s náhledem **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="33871-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="33871-231">Na stránce **Rezervace dávky** vyberte řádek pro dávku **B11** a pak vyberte **Řádek rezervace**.</span><span class="sxs-lookup"><span data-stu-id="33871-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="33871-232">V průběhu automatické rezervace není určena žádná logika pro přiřazování skladových míst a registračních značek.</span><span class="sxs-lookup"><span data-stu-id="33871-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="33871-233">Množství lze ručně zadat do pole **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="33871-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="33871-234">Všimněte si, že na záložce s náhledem **Čísla dávek potvrzená pro řádek zdroje** se zobrazí dávka **B11** jako **Potvrzená**.</span><span class="sxs-lookup"><span data-stu-id="33871-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Potvrzení konkrétního čísla dávky na řádek prodejní objednávky na stránce rezervace dávky](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="33871-236">Rezervaci množství na řádku prodejní objednávky lze provést ve více dávkách.</span><span class="sxs-lookup"><span data-stu-id="33871-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="33871-237">Stejně tak lze provést rezervaci stejné dávky proti několika místům a registračním značkám (pokud jsou pro skladová místa povoleny registrační značky).</span><span class="sxs-lookup"><span data-stu-id="33871-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="33871-238">Rezervace konkrétní dávky pro množství na řádku prodejní objednávky může být také částečná.</span><span class="sxs-lookup"><span data-stu-id="33871-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="33871-239">Například celkové množství 100 jednotek může být rezervováno tak, aby určitá dávka byla potvrzena na 20 jednotek, zatímco 80 jednotek je rezervováno na pracovišti a na úrovni skladů pro všechny dostupné dávky.</span><span class="sxs-lookup"><span data-stu-id="33871-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="33871-240">V tomto případě bude WMS zpracovávat operace výdeje pomocí dvou oddělených řádků práce.</span><span class="sxs-lookup"><span data-stu-id="33871-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="33871-241">Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="33871-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="33871-242">Vyberte položku a poté vyberte **Spravovat zásoby** \> **Zobrazení** \> **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="33871-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Rezervace potvrzená objednávkou jako typ skladové transakce](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="33871-244">Zkontrolujte skladové transakce položky, které souvisejí s rezervací řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="33871-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="33871-245">Transakce, ve které je pole **Odkaz** nastaveno na **Prodejní objednávka** a pole **Výdej** je nastaveno **Rezervované – fyzicky** představuje rezervaci řádku objednávky pro dimenze zásob nad úrovní **skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="33871-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="33871-246">Podle hierarchie rezervací zásob položky jsou tyto dimenze pracoviště, sklad a stav zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="33871-247">Transakce, ve které je pole **Odkaz** nastaveno na **Rezervace potvrzená objednávkou** a pole **Výdej** je nastaveno **Rezervované – fyzicky** představuje rezervaci řádku objednávky pro specifickou dávku a pro všechny dimenze zásob nad ní.</span><span class="sxs-lookup"><span data-stu-id="33871-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="33871-248">Podle hierarchie rezervací zásob položky jsou tyto dimenze číslo dávky a skladové místo.</span><span class="sxs-lookup"><span data-stu-id="33871-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="33871-249">V tomto příkladu je skladové místo **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="33871-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="33871-250">V záhlaví prodejní objednávky vyberte **Sklad** \> **Akce** \> **Uvolnění do skladu**.</span><span class="sxs-lookup"><span data-stu-id="33871-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="33871-251">Řádek objednávky je nyní ve vlně a vytvoří se vytížení a práce.</span><span class="sxs-lookup"><span data-stu-id="33871-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="33871-252">Kontrola a zpracování práci skladu s čísly dávek potvrzených objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="33871-253">Na záložce s náhledem **Řádky prodejní objednávky** zvolte **Sklad** \> **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="33871-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="33871-254">Práce, která zpracovává operaci výdeje pro množství dávky potvrzené v řádku prodejní objednávky, má následující charakteristiky:</span><span class="sxs-lookup"><span data-stu-id="33871-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="33871-255">Chcete-li vytvořit práci, systém použije šablony práce, ale ne směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="33871-256">Chcete-li určit, kdy má být vytvořena nová práce, bude použito standardní nastavení definované pro šablony práce, jako je například maximální počet řádků výdeje nebo určitá měrná jednotka.</span><span class="sxs-lookup"><span data-stu-id="33871-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="33871-257">Pravidla, která jsou spojena se směrnicemi skladových míst pro určení skladových místa výdeje, však nejsou zvažována, protože rezervace potvrzená objednávkou již určuje všechny dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="33871-258">Tyto dimenze zásob obsahují dimenze na úrovni skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="33871-259">Tato práce tedy tyto dimenze zdědí bez nutnosti konzultovat směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="33871-260">Číslo dávky není zobrazeno na řádku výdeje (jako je například případ pro řádek práce vytvořený pro položku, která má přidruženou hierarchii rezervace Batch-above\[location\].) Místo toho se v poli "od" číslo dávky a všechny ostatní dimenze uskladnění zobrazí na skladové transakci řádku práce, která je odkazována z přidružených skladových transakcí.</span><span class="sxs-lookup"><span data-stu-id="33871-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Skladová transakce pro práci, která pochází z rezervace potvrzené objednávkou](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="33871-262">Po vytvoření práce se skladová transakce položky, kde je pole **Odkaz** nastaveno na **Rezervace potvrzená objednávkou**, odstraní.</span><span class="sxs-lookup"><span data-stu-id="33871-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="33871-263">Skladová transakce, kde je pole **Odkaz** nastaveno na **Práce**, nyní ukládá fyzickou rezervaci ve všech dimenzích zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="33871-264">Skladové operace mohou pokračovat v provádění práce obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="33871-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="33871-265">Pokyny v mobilním zařízení však nařídí pracovníkovi, aby vydával určité číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="33871-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="33871-266">V prostředích skladu, kde jsou skladová místa řízena registrační značkou, poté, co pracovník dostane do skladového místa, kde je uložena stejná dávka na více registračních štítků, může vybírat z libovolné registrační značky, která ještě není rezervována (například jinou rezervace nebo práce potvrzené objednávkou, která pochází z rezervace daného typu.)</span><span class="sxs-lookup"><span data-stu-id="33871-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="33871-267">Pokud z místa uvedeného na řádku práce odcházíte k vyskladnění, mohou operátoři skladu použít jednu z následujících akcí, které přesměrují výběr konkrétní dávky z vhodnějšího umístění:</span><span class="sxs-lookup"><span data-stu-id="33871-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="33871-268">Standardní akce **Přepsat umístění** na mobilním zařízení (za předpokladu, že je nastavení **Umožnit přepis výdejního umístění** pracovníka skladu povoleno)</span><span class="sxs-lookup"><span data-stu-id="33871-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="33871-269">Akce **Změnit umístění** na stránce **Podrobnosti seznamu práce**.</span><span class="sxs-lookup"><span data-stu-id="33871-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="33871-270">V mobilním zařízení dokončete výdej a vklad práce.</span><span class="sxs-lookup"><span data-stu-id="33871-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="33871-271">Množství **10** pro číslo dávky **B11** je nyní vyskladněno pro řádek prodejní objednávky a je vloženo do umístění **Portál**.</span><span class="sxs-lookup"><span data-stu-id="33871-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="33871-272">V tomto okamžiku je vše připraveno k naložení na nákladní vůz a odesláno na adresu odběratele.</span><span class="sxs-lookup"><span data-stu-id="33871-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="33871-273">Flexibilní rezervace registrační značky</span><span class="sxs-lookup"><span data-stu-id="33871-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="33871-274">Scénáře obchodu</span><span class="sxs-lookup"><span data-stu-id="33871-274">Business scenario</span></span>

<span data-ttu-id="33871-275">V tomto scénáři společnost používá řízení skladu a zpracování práce a zpracovává plánování nákladu na úrovni jednotlivých palet / kontejnerů mimo Supply Chain Management před vytvořením práce.</span><span class="sxs-lookup"><span data-stu-id="33871-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="33871-276">Tyto kontejnery jsou reprezentovány registračními značkami v rozměrech inventáře.</span><span class="sxs-lookup"><span data-stu-id="33871-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="33871-277">Proto pro tento přístup musí být před objednáním předběžně přiřazeny řádky prodejních objednávek specifické registrační značky.</span><span class="sxs-lookup"><span data-stu-id="33871-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="33871-278">Společnost hledá flexibilitu ve způsobu zacházení s pravidly rezervace registračních značek, aby došlo k následujícímu chování:</span><span class="sxs-lookup"><span data-stu-id="33871-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="33871-279">Registrační značku lze zaznamenat a rezervovat, když je objednávka provedena, zpracovatelem prodeje, a nelze ji pořídit jinými požadavky.</span><span class="sxs-lookup"><span data-stu-id="33871-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="33871-280">Toto chování pomáhá zaručit, že plánovaná registrační značka je expedována odběrateli.</span><span class="sxs-lookup"><span data-stu-id="33871-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="33871-281">Pokud registrační značka ještě není přiřazena k řádku prodejní objednávky, pracovníci skladu mohou při vyskladnění po dokončení registrace a rezervace prodejní objednávky vybrat poznávací značku.</span><span class="sxs-lookup"><span data-stu-id="33871-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="33871-282">Zapnutí flexibilní rezervace registrační značky</span><span class="sxs-lookup"><span data-stu-id="33871-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="33871-283">Než můžete použít flexibilní rezervaci registrační značky, musíte v systému zapnout dvě funkce.</span><span class="sxs-lookup"><span data-stu-id="33871-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="33871-284">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav těchto funkcí a dle potřeby je zapnout.</span><span class="sxs-lookup"><span data-stu-id="33871-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="33871-285">Funkce musíte zapnout v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="33871-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="33871-286">**Název funkce:** *Flexibilní rezervace dimenze na úrovni skladu*</span><span class="sxs-lookup"><span data-stu-id="33871-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="33871-287">**Název funkce:** *Flexibilní rezervace registrační značky dle objednávky*</span><span class="sxs-lookup"><span data-stu-id="33871-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="33871-288">Na prodejní objednávce si rezervujte konkrétní registrační značku</span><span class="sxs-lookup"><span data-stu-id="33871-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="33871-289">Chcete-li v objednávce povolit rezervaci registrační značky, musíte zaškrtnout políčko **Povolit rezervaci na objednávce poptávky** pro úroveň **Registrační značka** na stránce **Hierarchie rezervace zásob** pro hierarchii, která je spojena s příslušnou položkou.</span><span class="sxs-lookup"><span data-stu-id="33871-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Stránka hierarchií rezervace zásob pro flexibilní hierarchii rezervace poznávacích značek](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="33871-291">Rezervace registrační značky můžete v objednávce povolit kdykoli v místě nasazení.</span><span class="sxs-lookup"><span data-stu-id="33871-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="33871-292">Tato změna neovlivní žádné rezervace nebo otevřené práce skladu, které byly vytvořeny před provedením změny.</span><span class="sxs-lookup"><span data-stu-id="33871-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="33871-293">Nemůžete vša zrušit zaškrtnutí políčka **Povolit rezervaci na objednávce poptávky**, pokud pro jednu nebo více položek které jsou přidruženy k dané hierarchii rezervací, existují otevřené odchozí transakce zásob typů výdeje, které mají stav *Na objednávce*, *Rezervováno objednáno* nebo *Rezervováno fyzicky*.</span><span class="sxs-lookup"><span data-stu-id="33871-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="33871-294">I když je zaškrtnuto políčko **Povolit rezervaci na objednávku poptávky** pro úroveň **Registrační značka**, je to stále možné *nerezervovat* konkrétní registrační značku na objednávce.</span><span class="sxs-lookup"><span data-stu-id="33871-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="33871-295">V tomto případě se použije výchozí logika operací skladu, která je platná pro hierarchii rezervace.</span><span class="sxs-lookup"><span data-stu-id="33871-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="33871-296">Chcete-li rezervovat konkrétní registrační značku, musíte použít proces [Otevřený datový protokol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md). V aplikaci můžete provést tuto rezervaci přímo z prodejní objednávky pomocí možnosti **Rezervace vázaná na objednávku dle registrační značky** v příkazu **Otevřít v Excelu**.</span><span class="sxs-lookup"><span data-stu-id="33871-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="33871-297">V datech entity, která se otevírají v doplňku Excel, musíte zadat následující data související s rezervací a poté vybrat **Publikovat**, chcete-li poslat data zpět do Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="33871-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="33871-298">Reference (Pouze hodnota *Prodejní objednávka* je podporována.)</span><span class="sxs-lookup"><span data-stu-id="33871-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="33871-299">Číslo objednávky (Hodnota může být odvozena ze šarže.)</span><span class="sxs-lookup"><span data-stu-id="33871-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="33871-300">ID šarže</span><span class="sxs-lookup"><span data-stu-id="33871-300">Lot ID</span></span>
- <span data-ttu-id="33871-301">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="33871-301">License plate</span></span>
- <span data-ttu-id="33871-302">Množství</span><span class="sxs-lookup"><span data-stu-id="33871-302">Quantity</span></span>

<span data-ttu-id="33871-303">Pokud musíte vyhradit konkrétní registrační značku pro dávkově sledovanou položku, použijte stránku **Dávková rezervace**, jak je popsáno v sekci [Zadejte podrobnosti o prodejní objednávce](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="33871-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="33871-304">Když je řádek prodejní objednávky, který používá rezervaci registrační značky potvrzené objednávkou, zpracován operacemi skladu, nebudou použity direktivy o umístění.</span><span class="sxs-lookup"><span data-stu-id="33871-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="33871-305">Pokud se pracovní položka ve skladu skládá z řádků, které se rovnají celé paletě a mají množství potvrzené registrační značkou, můžete optimalizovat proces vyskladnění pomocí položky nabídky mobilního zařízení, kde je možnost **Manipulovat pomocí registrační značky** nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="33871-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="33871-306">Pracovník skladu pak může naskenovat poznávací značku, aby dokončil výběr, aniž by musel skenovat položky z práce jednu po druhé.</span><span class="sxs-lookup"><span data-stu-id="33871-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Položka nabídky mobilního zařízení, kde je volba Zpracovat podle registrační značky nastavena na Ano](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="33871-308">Protože funkce **Zpracovat podle registrační značky** nepodporuje práci, která pokrývá více palet, je lepší mít samostatnou pracovní položku pro různé registrační značky.</span><span class="sxs-lookup"><span data-stu-id="33871-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="33871-309">Chcete-li použít tento přístup, přidejte pole **ID poznávací značky vázané na objednávku** jako konec pracovní hlavičky na stránce **Pracovní šablona**.</span><span class="sxs-lookup"><span data-stu-id="33871-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="33871-310">Příklad scénáře: Nastavte a zpracujte rezervaci registrační značky vázané na objednávku</span><span class="sxs-lookup"><span data-stu-id="33871-310">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="33871-311">Tento scénář ukazuje, jak nastavit a zpracovat rezervaci registrační značky vázané na objednávku.</span><span class="sxs-lookup"><span data-stu-id="33871-311">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="33871-312">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="33871-312">Make demo data available</span></span>

<span data-ttu-id="33871-313">Tento scénář odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33871-313">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="33871-314">Chcete-li s tímto scénářem pracovat pomocí hodnot zde poskytnutých, musíte používat prostředí, ve kterém jsou nainstalována ukázková data.</span><span class="sxs-lookup"><span data-stu-id="33871-314">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="33871-315">Kromě toho musíte dříve, než začnete, nastavit právnickou osobu na **USMF**.</span><span class="sxs-lookup"><span data-stu-id="33871-315">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="33871-316">Vytvořte hierarchii rezervace inventáře, která umožňuje rezervaci poznávací značky</span><span class="sxs-lookup"><span data-stu-id="33871-316">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="33871-317">Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Hierarchie rezervací.**</span><span class="sxs-lookup"><span data-stu-id="33871-317">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="33871-318">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="33871-318">Select **New**.</span></span>
1. <span data-ttu-id="33871-319">Do pole **Název** zadejte hodnotu (například *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="33871-319">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="33871-320">Do pole **Popis** zadejte hodnotu (například *Flexibilní rezervace registrační značky*).</span><span class="sxs-lookup"><span data-stu-id="33871-320">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="33871-321">V seznamu **Vybraný** vyberte **Číslo šarže**, **Sériové číslo** a **Vlastník**.</span><span class="sxs-lookup"><span data-stu-id="33871-321">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="33871-322">Vyberte tlačítko **Odebrat** ![šipka zpět](media/backward-button.png) a přesuňte vybrané záznamy do seznamu **K dispozici**.</span><span class="sxs-lookup"><span data-stu-id="33871-322">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="33871-323">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="33871-323">Select **OK**.</span></span>
1. <span data-ttu-id="33871-324">V řádku pro úroveň dimenze **Registrační značka** zaškrtněte políčko **Povolit rezervaci na objednávce poptávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-324">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="33871-325">Úroveň **Umístění** je vybrána automaticky a nelze u ní zrušit zaškrtávací políčko.</span><span class="sxs-lookup"><span data-stu-id="33871-325">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="33871-326">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="33871-326">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="33871-327">Vytvoření dvou uvolněných produktů</span><span class="sxs-lookup"><span data-stu-id="33871-327">Create two released products</span></span>

1. <span data-ttu-id="33871-328">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="33871-328">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="33871-329">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="33871-329">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="33871-330">V dialogovém okně **Nový uvolněný produkt** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="33871-330">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="33871-331">**Číslo produktu:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="33871-331">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="33871-332">**Číslo položky:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="33871-332">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="33871-333">**Skupina modelů položek:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="33871-333">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="33871-334">**Skupina položek:** *Audio*</span><span class="sxs-lookup"><span data-stu-id="33871-334">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="33871-335">**Skupina dimenze úložiště:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="33871-335">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="33871-336">**Skupina sledovací dimenze:** *Žádná*</span><span class="sxs-lookup"><span data-stu-id="33871-336">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="33871-337">**Hierarchie rezervace:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="33871-337">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="33871-338">Vyberte **OK**, produkt se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="33871-338">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="33871-339">Nový produkt je otevřen.</span><span class="sxs-lookup"><span data-stu-id="33871-339">The new product is opened.</span></span> <span data-ttu-id="33871-340">Na záložce s náhledem **Sklad** nastavte pole **ID skupiny pořadí jednotek** na hodnotu *ks*.</span><span class="sxs-lookup"><span data-stu-id="33871-340">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="33871-341">Opakujte předchozí kroky a vytvořte druhý produkt, který má stejná nastavení, ale nastavte **Číslo produktu** a **Číslo položky** na *Item2*.</span><span class="sxs-lookup"><span data-stu-id="33871-341">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="33871-342">V podokně Akce na kartě **Správa zásob** ve skupině **Zobrazit** vyberte **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="33871-342">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="33871-343">Poté vyberte **Úprava množství**.</span><span class="sxs-lookup"><span data-stu-id="33871-343">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="33871-344">Upravte zásoby na skladě nových položek podle pokynů v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="33871-344">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="33871-345">Zboží</span><span class="sxs-lookup"><span data-stu-id="33871-345">Item</span></span>  | <span data-ttu-id="33871-346">Sklad</span><span class="sxs-lookup"><span data-stu-id="33871-346">Warehouse</span></span> | <span data-ttu-id="33871-347">Skl. místo</span><span class="sxs-lookup"><span data-stu-id="33871-347">Location</span></span> | <span data-ttu-id="33871-348">Poznávací značka</span><span class="sxs-lookup"><span data-stu-id="33871-348">License plate</span></span> | <span data-ttu-id="33871-349">Množství</span><span class="sxs-lookup"><span data-stu-id="33871-349">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="33871-350">Item1</span><span class="sxs-lookup"><span data-stu-id="33871-350">Item1</span></span> | <span data-ttu-id="33871-351">24</span><span class="sxs-lookup"><span data-stu-id="33871-351">24</span></span>        | <span data-ttu-id="33871-352">FL-010</span><span class="sxs-lookup"><span data-stu-id="33871-352">FL-010</span></span>   | <span data-ttu-id="33871-353">LP01</span><span class="sxs-lookup"><span data-stu-id="33871-353">LP01</span></span>          | <span data-ttu-id="33871-354">10</span><span class="sxs-lookup"><span data-stu-id="33871-354">10</span></span>       |
    | <span data-ttu-id="33871-355">Item1</span><span class="sxs-lookup"><span data-stu-id="33871-355">Item1</span></span> | <span data-ttu-id="33871-356">24</span><span class="sxs-lookup"><span data-stu-id="33871-356">24</span></span>        | <span data-ttu-id="33871-357">FL-011</span><span class="sxs-lookup"><span data-stu-id="33871-357">FL-011</span></span>   | <span data-ttu-id="33871-358">LP02</span><span class="sxs-lookup"><span data-stu-id="33871-358">LP02</span></span>          | <span data-ttu-id="33871-359">10</span><span class="sxs-lookup"><span data-stu-id="33871-359">10</span></span>       |
    | <span data-ttu-id="33871-360">Item2</span><span class="sxs-lookup"><span data-stu-id="33871-360">Item2</span></span> | <span data-ttu-id="33871-361">24</span><span class="sxs-lookup"><span data-stu-id="33871-361">24</span></span>        | <span data-ttu-id="33871-362">FL-010</span><span class="sxs-lookup"><span data-stu-id="33871-362">FL-010</span></span>   | <span data-ttu-id="33871-363">LP01</span><span class="sxs-lookup"><span data-stu-id="33871-363">LP01</span></span>          | <span data-ttu-id="33871-364">5</span><span class="sxs-lookup"><span data-stu-id="33871-364">5</span></span>        |
    | <span data-ttu-id="33871-365">Item2</span><span class="sxs-lookup"><span data-stu-id="33871-365">Item2</span></span> | <span data-ttu-id="33871-366">24</span><span class="sxs-lookup"><span data-stu-id="33871-366">24</span></span>        | <span data-ttu-id="33871-367">FL-011</span><span class="sxs-lookup"><span data-stu-id="33871-367">FL-011</span></span>   | <span data-ttu-id="33871-368">LP02</span><span class="sxs-lookup"><span data-stu-id="33871-368">LP02</span></span>          | <span data-ttu-id="33871-369">5</span><span class="sxs-lookup"><span data-stu-id="33871-369">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="33871-370">Musíte vytvořit dvě poznávací značky a použít umístění, která umožňují smíšené položky, například *FL-010* a *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="33871-370">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="33871-371">Vytvořte prodejní objednávku a rezervujte konkrétní registrační značku</span><span class="sxs-lookup"><span data-stu-id="33871-371">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="33871-372">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="33871-372">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="33871-373">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="33871-373">Select **New**.</span></span>
1. <span data-ttu-id="33871-374">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="33871-374">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="33871-375">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="33871-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="33871-376">**Sklad:** *24*</span><span class="sxs-lookup"><span data-stu-id="33871-376">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="33871-377">Stisknutím **OK** zavřete dialogové okno **Vytvoření nákupní objednávky** a otevřete novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="33871-377">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="33871-378">Na pevné záložce **Řádky prodejní objednávky** přidejte řádek s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="33871-378">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="33871-379">**Číslo položky:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="33871-379">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="33871-380">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="33871-380">**Quantity:** *10*</span></span>

1. <span data-ttu-id="33871-381">Přidejte druhý řádek prodejní objednávky, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="33871-381">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="33871-382">**Číslo položky:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="33871-382">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="33871-383">**Množství:** *5*</span><span class="sxs-lookup"><span data-stu-id="33871-383">**Quantity:** *5*</span></span>

1. <span data-ttu-id="33871-384">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="33871-384">Select **Save**.</span></span>
1. <span data-ttu-id="33871-385">Na pevné záložce **Podrobnosti řádku** na kartě **Nastavení** si poznamenejte **ID šarže** pro každý řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-385">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="33871-386">Tyto hodnoty budou vyžadovány při rezervaci konkrétních poznávacích značek.</span><span class="sxs-lookup"><span data-stu-id="33871-386">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33871-387">Chcete-li rezervovat konkrétní poznávací značku, musíte použít datovou entitu **Rezervace vázaná na objednávku dle registrační značky**.</span><span class="sxs-lookup"><span data-stu-id="33871-387">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="33871-388">Chcete-li rezervovat dávkově sledovanou položku na konkrétní registrační značce, můžete také použít stránku **Dávková rezervace**, jak je popsáno v sekci [Zadejte podrobnosti o prodejní objednávce](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="33871-388">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="33871-389">Pokud zadáte poznávací značku přímo na řádku prodejní objednávky a potvrdíte ji do systému, nebude pro tuto linku použito řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-389">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="33871-390">Vyberte **Otevřít v Microsoft Office**, vyberte **Rezervace vázaná na objednávku dle registrační značky** a stáhněte si soubor.</span><span class="sxs-lookup"><span data-stu-id="33871-390">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="33871-391">V aplikaci Excel otevřete stažený soubor a zvolte **Povolit úpravy**. Tím povolíte spuštění doplňku aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="33871-391">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="33871-392">Pokud používáte doplněk aplikace Excel poprvé, zvolte možnost **Důvěřovat tomuto doplňku**.</span><span class="sxs-lookup"><span data-stu-id="33871-392">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="33871-393">Pokud se zobrazí výzva k přihlášení, zvolte **Přihlásit** a potom se přihlaste pomocí stejných pověření, jaká jste použili pro přihlášení k aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33871-393">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="33871-394">Chcete-li rezervovat položku na konkrétní registrační značce, v doplňku Excel vyberte **Nový** a přidejte řádek rezervace, Poté nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="33871-394">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="33871-395">**ID šarže:** Zadejte **ID šarže**, kterou jste našli pro řádek prodejní objednávky *Item1*.</span><span class="sxs-lookup"><span data-stu-id="33871-395">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="33871-396">**Registrační značka:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="33871-396">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="33871-397">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="33871-397">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="33871-398">Chcete-li přidat další řádek rezervace, klikněte na **Nový** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="33871-398">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="33871-399">**ID šarže:** Zadejte **ID šarže**, kterou jste našli pro řádek prodejní objednávky *Item2*.</span><span class="sxs-lookup"><span data-stu-id="33871-399">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="33871-400">**Registrační značka:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="33871-400">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="33871-401">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="33871-401">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="33871-402">V doplňku Excel vyberte **Publikovat** a pošlete data zpět do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33871-402">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33871-403">Rezervační řádek se v systému objeví, pouze pokud je publikování dokončeno bez chyb.</span><span class="sxs-lookup"><span data-stu-id="33871-403">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="33871-404">Přejděte zpět na Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33871-404">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="33871-405">Chcete-li zkontrolovat rezervaci položky, na pevné záložce **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte **Udržovat \> Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="33871-405">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="33871-406">Všimněte si, že pro řádek prodejní objednávky pro *Item1* jsou rezervovány zásoby v množství *10* a pro řádek prodejní objednávky pro *Item2* je vyhrazeno množství *5* zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-406">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="33871-407">Chcete-li zkontrolovat transakce inventáře, které souvisejí s rezervací řádku prodejní objednávky, na pevné záložce **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte **zobrazit \> Transakce**.</span><span class="sxs-lookup"><span data-stu-id="33871-407">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="33871-408">Všimněte si, že existují dvě transakce, které se vztahují k rezervaci: jedna, kde je pole **Odkaz** nastaveno na *Prodejní objednávka* a jedna, kde je pole **Odkaz** nastaveno na *Rezervace vázaná na objednávku*.</span><span class="sxs-lookup"><span data-stu-id="33871-408">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33871-409">Transakce, ve které je pole **Odkaz** nastaveno na *Prodejní objednávka* představuje rezervaci řádku objednávky pro dimenze zásob nad úrovní **skladového místa** (site, sklad a stav zásob).</span><span class="sxs-lookup"><span data-stu-id="33871-409">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="33871-410">Transakce, kde pole **Odkaz** je nastaveno na *Rezervace vázaná na objednávku*, představuje rezervaci řádku objednávky pro konkrétní registrační značku a umístění.</span><span class="sxs-lookup"><span data-stu-id="33871-410">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="33871-411">Chcete-li uvolnit prodejní objednávku, v pododokně akcí na kartě **Sklad** ve skupině **Akce** vyberte **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="33871-411">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="33871-412">Zkontrolujte a zpracujte práci ve skladu s přiřazenými registračními značkami</span><span class="sxs-lookup"><span data-stu-id="33871-412">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="33871-413">Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Sklad** vyberte možnost **Podrobnosti práce**.</span><span class="sxs-lookup"><span data-stu-id="33871-413">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="33871-414">Jako když se provádí rezervace pro konkrétní dávku, systém nepoužívá směrnice o umístění, když vytváří práci pro prodejní objednávku, která používá rezervaci poznávací značky.</span><span class="sxs-lookup"><span data-stu-id="33871-414">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="33871-415">Protože rezervace vázaná na objednávku specifikuje všechny dimenze zásob, včetně umístění, nemusí být použity direktivy o umístění, protože tyto dimenze zásob jsou právě zadány v práci.</span><span class="sxs-lookup"><span data-stu-id="33871-415">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="33871-416">Jsou uvedeny v sekci **Z dimenzí zásob** na stránce **Transakce pracovních zásob**.</span><span class="sxs-lookup"><span data-stu-id="33871-416">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33871-417">Po vytvoření práce se skladová transakce položky, kde je pole **Odkaz** nastaveno na *Rezervace potvrzená objednávkou*, odstraní.</span><span class="sxs-lookup"><span data-stu-id="33871-417">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="33871-418">Skladová transakce, kde je pole **Odkaz** nastaveno na *Práce*, nyní ukládá fyzickou rezervaci ve všech dimenzích zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-418">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="33871-419">Na mobilním zařízení dokončete výběr a umístěte práci pomocí položky nabídky, kde je zaškrtnuto políčko **Zpracovat podle registrační značky**.</span><span class="sxs-lookup"><span data-stu-id="33871-419">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="33871-420">Funkce **Zpracovat podle registrační značky** vám pomůže zpracovat celou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="33871-420">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="33871-421">Pokud musíte zpracovat část registrační značky, tuto funkci nemůžete použít.</span><span class="sxs-lookup"><span data-stu-id="33871-421">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="33871-422">Doporučujeme, abyste pro každou registrační značku vygenerovali samostatnou práci.</span><span class="sxs-lookup"><span data-stu-id="33871-422">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="33871-423">K dosažení tohoto výsledku použijte funkci **Konce pracovních hlaviček** na stránce **Pracovní šablona**.</span><span class="sxs-lookup"><span data-stu-id="33871-423">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="33871-424">Registrační značka *LP02* je nyní vyskladněna pro řádky prodejní objednávky a vložena do umístění *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="33871-424">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="33871-425">V tomto okamžiku je vše připraveno k naložení a odeslání odběrateli.</span><span class="sxs-lookup"><span data-stu-id="33871-425">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="33871-426">Zpracování výjimky práce skladu s čísly dávek potvrzených objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-426">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="33871-427">Práce na skladě pro výdej čísel dávek potvrzených objednávkou podléhá stejnému standardnímu zpracování výjimek a akcím při běžné práci.</span><span class="sxs-lookup"><span data-stu-id="33871-427">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="33871-428">Obecně platí, že otevřenou práci nebo řádek práce lze zrušit, lze je přerušit, protože skladovací místo uživatele je plné, může být krátkodobě vyskladněno a je aktualizovat z důvodu přesunu.</span><span class="sxs-lookup"><span data-stu-id="33871-428">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="33871-429">Stejně tak lze snížit vyskladněné množství práce, které již bylo dokončeno, nebo lze stornovat práci.</span><span class="sxs-lookup"><span data-stu-id="33871-429">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="33871-430">Následující pravidlo klíče se použije na všechny tyto akce zpracování výjimek: číslo dávky, které bylo rezervováno pro odběratele, nelze nikdy nahradit jiným číslem dávky, ale dimenze uskladnění (umístění a registrační značka) mohou být změněny buď pomocí Ruční aktualizace uživatelem nebo automatickou aktualizací systémem.</span><span class="sxs-lookup"><span data-stu-id="33871-430">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="33871-431">Automatická aktualizace je založena na stejném náhodném přiřazení dimenzí úložiště, které byly použity, když byla určitá dávka automaticky rezervována, ale nebyly zadány žádné dimenze úložiště.</span><span class="sxs-lookup"><span data-stu-id="33871-431">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="33871-432">Příklad</span><span class="sxs-lookup"><span data-stu-id="33871-432">Example scenario</span></span>

<span data-ttu-id="33871-433">Příkladem tohoto scénáře je situace, kdy je dříve dokončená práce vyzvednuta pomocí funkce **Snížit vyskladněné množství**.</span><span class="sxs-lookup"><span data-stu-id="33871-433">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="33871-434">Tento příklad předpokládá, že jste již provedli kroky popsané v části [Příklad scénáře: Přidělení čísla šarže](#Example-batch-allocation).</span><span class="sxs-lookup"><span data-stu-id="33871-434">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="33871-435">Z tohoto příkladu to pokračuje.</span><span class="sxs-lookup"><span data-stu-id="33871-435">It continues from that example.</span></span>

1. <span data-ttu-id="33871-436">Přejděte na **Řízení skladu** \> **Nakládky** \> **Aktivní nakládky**.</span><span class="sxs-lookup"><span data-stu-id="33871-436">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="33871-437">Vyberte nakládku, která byla vytvořena v souvislosti s dodávkou prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="33871-437">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="33871-438">Na záložce s náhledem **Naložit řádky objednávky** zvolte **Snížit vyskladněné množství**.</span><span class="sxs-lookup"><span data-stu-id="33871-438">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="33871-439">Na stránce **Snížit vyskladněné množství** vyberte v poli **Přesunout na místo** možnost **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="33871-439">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="33871-440">V poli **Přejít na registrační značku** zvolte **LP33**.</span><span class="sxs-lookup"><span data-stu-id="33871-440">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="33871-441">V mřížce v poli **Skladové množství ke zrušení výdeje** zadejte **10**.</span><span class="sxs-lookup"><span data-stu-id="33871-441">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="33871-442">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="33871-442">Select **OK**.</span></span>

<span data-ttu-id="33871-443">Zde jsou výsledky akce zrušení výdeje:</span><span class="sxs-lookup"><span data-stu-id="33871-443">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="33871-444">Stav dříve uzavřené práce je nastaven na **Zrušeno**.</span><span class="sxs-lookup"><span data-stu-id="33871-444">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="33871-445">Nová práce typu **Přesun zásob** se vytvoří pro nevyzvednuté množství **10** pro číslo dávky **B11**.</span><span class="sxs-lookup"><span data-stu-id="33871-445">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="33871-446">Tato práce představuje přesun z místa **Portál** na registrační značku **LP33** v umístění **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="33871-446">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="33871-447">Stav je nastaven na **Zavřeno**.</span><span class="sxs-lookup"><span data-stu-id="33871-447">The status is set to **Closed**.</span></span>
- <span data-ttu-id="33871-448">Systém znovu rezervuje číslo dávky, které bylo původně objednáno, a přiřadí ID umístění a registrační značky.</span><span class="sxs-lookup"><span data-stu-id="33871-448">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="33871-449">(Tento proces odpovídá spuštění funkce **Rezervovat řádek** pro řádek objednávky pro dané číslo dávky).</span><span class="sxs-lookup"><span data-stu-id="33871-449">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="33871-450">Výsledkem je, že se dávka **B11** zobrazí jako potvrzená na záložce s náhledem **Čísla dávek potvrzená pro řádek zdroje** na stránce **Rezervace dávky**, a pole **Rezervace** obsahuje množství **10** pro číslo dávky **B11**.</span><span class="sxs-lookup"><span data-stu-id="33871-450">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="33871-451">Dále je pole **Místo** nastaveno na **FL-001** a pole **Registrační značka** je nastaveno na **LP11**.</span><span class="sxs-lookup"><span data-stu-id="33871-451">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="33871-452">(Tato pole můžete přidat do mřížky, pokud nejsou viditelná.)</span><span class="sxs-lookup"><span data-stu-id="33871-452">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="33871-453">V následujících tabulkách je uveden přehled, který zobrazuje způsob, jakým systém zpracovává rezervace dávky potvrzené objednávkou pro určité akce skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-453">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="33871-454">Chcete-li interpretovat obsah v tabulkách, předpokládejme, že každá akce skladu je spuštěna v kontextu existující práce ve skladu, která pochází z rezervace dávky potvrzené objednávkou, nebo že provádění jednotlivých akcí skladu ovlivňuje práci tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="33871-454">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="33871-455">V těchto tabulkách sloupec "množství dávky je k dispozici" označuje, zda množství dávky k dispozici kromě množství, které již bylo rezervováno pro aktuální potvrzené rezervace nebo již rezervované pro práci ve skladu pochází z rezervací daného typu.</span><span class="sxs-lookup"><span data-stu-id="33871-455">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="33871-456">Přepsání místa výdeje na otevřené práci</span><span class="sxs-lookup"><span data-stu-id="33871-456">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-457">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-457">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-458">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-458">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-459">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-459">Key user steps</span></span></th>
<th><span data-ttu-id="33871-460">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-460">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-461">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-461">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="33871-462">Možnost <strong>Umožnit přepis výdejního umístění</strong> je povolena na pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="33871-462">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="33871-463">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-463">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-464">Vyberte položku nabídky <strong>Přepsat umístění</strong> v aplikaci skladu při zahájení práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-464">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="33871-465">Vyberte <strong>Navrhnout</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-465">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="33871-466">Potvrďte nové skladové místo navrhované na základě dostupnosti množství dávky.</span><span class="sxs-lookup"><span data-stu-id="33871-466">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-467">Při aktuální práci dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="33871-467">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="33871-468">Místo na řádku výdeje je aktualizováno na nové místo.</span><span class="sxs-lookup"><span data-stu-id="33871-468">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="33871-469">(Je-li toto umístění řízeno registrační značkou, je k skladové transakci práce přiřazena náhodná registrační značka a pracovník může vybírat z registračních značek, které mají dostupné množství.)</span><span class="sxs-lookup"><span data-stu-id="33871-469">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="33871-470">Pokud se množství nachází na více než jedné registrační značce v novém skladovém místě, bude původní řádek výdeje rozdělen do několika řádků tak, aby souhlasila každá registrační značka.</span><span class="sxs-lookup"><span data-stu-id="33871-470">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-471">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-471">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-472">Žádný</span><span class="sxs-lookup"><span data-stu-id="33871-472">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-473">Vyberte položku nabídky <strong>Přepsat umístění</strong> v aplikaci skladu při zahájení práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-473">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="33871-474">Zadat ručně místo.</span><span class="sxs-lookup"><span data-stu-id="33871-474">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-475">Akce <strong>Přepsání místa</strong> není možná.</span><span class="sxs-lookup"><span data-stu-id="33871-475">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="33871-476">Dojde k selhání a dojde k vyvolání chyby.</span><span class="sxs-lookup"><span data-stu-id="33871-476">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="33871-477">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-477">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="33871-478">Tlačítko Úplné – rozdělení řádku práce z důvodu přetečení v umístění uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-478">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-479">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-479">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-480">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-480">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-481">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-481">Key user steps</span></span></th>
<th><span data-ttu-id="33871-482">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-482">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-483">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-483">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33871-484">Možnost <strong>Povolit rozdělení práce</strong> je povolena na položce nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="33871-484">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="33871-485">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-485">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-486">Vyberte položku nabídky <strong>Úplný</strong> v aplikaci skladu při zpracování práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-486">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="33871-487">Do pole <strong>Vyskladněné množství</strong> zadejte částečné množství požadovaného výdeje, které označuje plnou kapacitu.</span><span class="sxs-lookup"><span data-stu-id="33871-487">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="33871-488">Při aktuální práci je množství aktualizováno na zbývající množství, které musí být vyskladněno.</span><span class="sxs-lookup"><span data-stu-id="33871-488">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="33871-489">Nová práce pro vyskladněné množství je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="33871-489">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="33871-490">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-490">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="33871-491">Snížení vyskladněného množství dokončené práce (z nákladu)</span><span class="sxs-lookup"><span data-stu-id="33871-491">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-492">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-492">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-493">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-493">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-494">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-494">Key user steps</span></span></th>
<th><span data-ttu-id="33871-495">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-495">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-496">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-496">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="33871-497">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-497">Not applicable</span></span></td>
<td><span data-ttu-id="33871-498">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-498">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-499">Otevřete stránku <strong>Snížit vyskladněné množství</strong> z řádku vytížení.</span><span class="sxs-lookup"><span data-stu-id="33871-499">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="33871-500">Zadejte úplné množství pro zrušení výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-500">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="33871-501">Vyberte přesun do místa / na registrační značku.</span><span class="sxs-lookup"><span data-stu-id="33871-501">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="33871-502">Práce, která je přidružená k řádku vytížení, je zrušena.</span><span class="sxs-lookup"><span data-stu-id="33871-502">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="33871-503">Nová práce pro přesun zásob je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="33871-503">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-504">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-504">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="33871-505">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-505">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-506">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-506">No</span></span></td>
<td><span data-ttu-id="33871-507">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-507">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-508">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-508">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-509">Množství je znovu rezervováno pro stejnou dávku a pro stejné skladové místo a registrační značku (jedná-li se o místo řízené registrační značkou), které byly zadány při zrušení výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-509">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="33871-510">Přesunutí položky v rámci skladu</span><span class="sxs-lookup"><span data-stu-id="33871-510">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="33871-511">Tuto akci skladu lze použít pouze pro přesun typu **Proces pro vytvoření práce**, nikoli pro přesun podle šablony.</span><span class="sxs-lookup"><span data-stu-id="33871-511">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-512">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-512">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-513">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-513">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-514">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-514">Key user steps</span></span></th>
<th><span data-ttu-id="33871-515">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-515">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-516">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-516">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="33871-517">Možnost <strong>Povolit pohyb zásob s přidruženou prací</strong> je povolena u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="33871-517">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="33871-518">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-518">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-519">Zahajte přesun v aplikaci skladu.</span><span class="sxs-lookup"><span data-stu-id="33871-519">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="33871-520">Zadejte místa z a do.</span><span class="sxs-lookup"><span data-stu-id="33871-520">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="33871-521">Ve všech existujících pracích, které jsou přesunutím ovlivněny, se skladové místo výdeje aktualizuje na nové umístění "do".</span><span class="sxs-lookup"><span data-stu-id="33871-521">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="33871-522">Nová práce pro přesun zásob je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="33871-522">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-523">Všechny stávající rezervace, které jsou ovlivněny pohybem množství z daného skladového místa, budou znovu rezervovány pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-523">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="33871-524">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-524">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-525">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-525">No</span></span></td>
<td><span data-ttu-id="33871-526">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-526">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-527">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-527">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-528">Všechny stávající rezervace, které jsou ovlivněny pohybem množství z daného skladového místa, jsou znovu rezervovány pro stejnou dávku a pro nové umístění "do" a registrační značku (pokud je toto umístění řízeno registrační značkou).</span><span class="sxs-lookup"><span data-stu-id="33871-528">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="33871-529">Rezervace vyskladněného množství dokončené práce (z nákladu nebo vlny)</span><span class="sxs-lookup"><span data-stu-id="33871-529">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-530">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-530">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-531">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-531">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-532">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-532">Key user steps</span></span></th>
<th><span data-ttu-id="33871-533">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-533">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-534">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-534">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="33871-535">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-535">Not applicable</span></span></td>
<td><span data-ttu-id="33871-536">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-536">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-537">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-537">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="33871-538">Na stránce s požadavkem vyberte možnost <strong>Ponechat položky v aktuálním umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-538">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-539">Veškerá práce, která je přidružená k řádku vytížení, je zrušena.</span><span class="sxs-lookup"><span data-stu-id="33871-539">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="33871-540">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-540">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="33871-541">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-541">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-542">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-542">No</span></span></td>
<td><span data-ttu-id="33871-543">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-543">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-544">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-544">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-545">Množství je znovu rezervováno pro stejnou dávku a pro místo a registrační značku, kde bylo množství ponecháno při stornování.</span><span class="sxs-lookup"><span data-stu-id="33871-545">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-546">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-546">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-547">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-547">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="33871-548">Na stránce s požadavkem vyberte možnost <strong>Přiřadit položky k tomuto umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-548">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="33871-549">Aktuální práce je zrušena.</span><span class="sxs-lookup"><span data-stu-id="33871-549">The current work is canceled.</span></span></li>
<li><span data-ttu-id="33871-550">Nová práce pro přesun zásob je vytvořena a uzavřena.</span><span class="sxs-lookup"><span data-stu-id="33871-550">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-551">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-551">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="33871-552">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-552">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-553">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-553">No</span></span></td>
<td><span data-ttu-id="33871-554">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-554">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-555">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-555">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-556">Množství je znovu rezervováno pro stejnou dávku a pro místo a registrační značku, kterým bylo množství přiřazeno při stornování.</span><span class="sxs-lookup"><span data-stu-id="33871-556">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-557">Ano/Ne</span><span class="sxs-lookup"><span data-stu-id="33871-557">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-558">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-558">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="33871-559">Na stránce s požadavkem vyberte možnost <strong>Přesunout položky do tohoto umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-559">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-560">Storno není podporováno.</span><span class="sxs-lookup"><span data-stu-id="33871-560">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="33871-561">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-561">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-562">Ano/Ne</span><span class="sxs-lookup"><span data-stu-id="33871-562">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-563">Otevřete stránku <strong>Stornovat práci</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-563">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="33871-564">Na stránce s požadavkem vyberte možnost <strong>Přesunout položky podle směrnic skladového umístění</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-564">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-565">Storno není podporováno.</span><span class="sxs-lookup"><span data-stu-id="33871-565">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="33871-566">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-566">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="33871-567">Krátkodobý výdej a množství – Zaregistrujte množství jako fyzicky nenalezené nav místě nebo na registrační značce během provádění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-567">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-568">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-568">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-569">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-569">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-570">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-570">Key user steps</span></span></th>
<th><span data-ttu-id="33871-571">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-571">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-572">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-572">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="33871-573">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Žádný</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-573">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="33871-574">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-574">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-575">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-575">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="33871-576">Do pole <strong>Vyskladněné množství</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-576">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="33871-577">Do pole <strong>Důvod</strong> zadejte <strong>Žádné opakované přidělení</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-577">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="33871-578">Aktuální práce je uzavřena a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-578">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="33871-579">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="33871-579">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-580">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-580">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="33871-581">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-581">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-582">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-582">No</span></span></td>
<td><span data-ttu-id="33871-583">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-583">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="33871-584">Akce krátkodobého výdeje se nezdaří a dojde k vyvolání chyby.</span><span class="sxs-lookup"><span data-stu-id="33871-584">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="33871-585">Aktuální práce zůstane otevřená.</span><span class="sxs-lookup"><span data-stu-id="33871-585">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-586">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-586">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="33871-587">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Žádný</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-587">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="33871-588">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-588">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-589">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-589">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="33871-590">Do pole <strong>Vyskladněné množství</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-590">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="33871-591">Do pole <strong>Důvod</strong> zadejte <strong>Žádné opakované přidělení</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-591">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="33871-592">Aktuální práce je uzavřena a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-592">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="33871-593">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="33871-593">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-594">Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě krátkodobého výdeje, budou znovu rezervovány pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-594">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="33871-595">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-595">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-596">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-596">No</span></span></td>
<td><span data-ttu-id="33871-597">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-597">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-598">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-598">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-599">Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě krátkodobého výdeje, budou odstraněny.</span><span class="sxs-lookup"><span data-stu-id="33871-599">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-600">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne/Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-600">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="33871-601">Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="33871-601">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="33871-602">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-602">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-603">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-603">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="33871-604">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-604">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="33871-605">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-605">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="33871-606">V seznamu vyberte umístění/registrační značku.</span><span class="sxs-lookup"><span data-stu-id="33871-606">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="33871-607">Při aktuální práci dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="33871-607">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="33871-608">Řádek výdeje je uzavřen a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-608">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="33871-609">Řádek vložení je zrušen.</span><span class="sxs-lookup"><span data-stu-id="33871-609">The put line is canceled.</span></span></li>
<li><span data-ttu-id="33871-610">Je vytvořen nový řádek vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="33871-610">A new pick line is created.</span></span> <span data-ttu-id="33871-611">Používá se místo / registrační značka, které uživatel vybral.</span><span class="sxs-lookup"><span data-stu-id="33871-611">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="33871-612">Je vytvořen nový řádek vložení.</span><span class="sxs-lookup"><span data-stu-id="33871-612">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="33871-613">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="33871-613">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-614">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-614">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-615">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-615">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="33871-616">Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="33871-616">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="33871-617">Žádný</span><span class="sxs-lookup"><span data-stu-id="33871-617">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-618">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-618">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="33871-619">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-619">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="33871-620">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-620">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-621">Akce krátkodobého výdeje se nezdaří a dojde k vyvolání chyby.</span><span class="sxs-lookup"><span data-stu-id="33871-621">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="33871-622">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-622">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-623">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Ruční</strong>, <strong>Úprava zásob</strong> = <strong>Ano</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-623">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="33871-624">Kromě toho je povolena možnost <strong>Povolit ruční opakované přidělení zboží</strong> u pracovníka.</span><span class="sxs-lookup"><span data-stu-id="33871-624">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="33871-625">Žádný</span><span class="sxs-lookup"><span data-stu-id="33871-625">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-626">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-626">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="33871-627">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-627">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="33871-628">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s ručním opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-628">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="33871-629">V seznamu vyberte umístění/registrační značku.</span><span class="sxs-lookup"><span data-stu-id="33871-629">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="33871-630">Při aktuální práci dojde k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="33871-630">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="33871-631">Řádek výdeje je uzavřen a vyskladněné množství je 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-631">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="33871-632">Řádek vložení je zrušen.</span><span class="sxs-lookup"><span data-stu-id="33871-632">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="33871-633">Vytvoří se skladová transakce typu <strong>Inventura</strong> inventury a typ vydání <strong>Prodáno</strong> za účelem reprezentování úpravy.</span><span class="sxs-lookup"><span data-stu-id="33871-633">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="33871-634">Všechny stávající rezervace, které jsou ovlivněny úpravou množství v skladovém místě /registrační značce krátkodobého výdeje, budou odstraněny.</span><span class="sxs-lookup"><span data-stu-id="33871-634">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-635">Je nastavena výjimka práce typu <strong>krátkodobý výdej</strong>, kde <strong>Opakované přidělení zboží</strong> = <strong>Automatický</strong>, <strong>Úprava zásob</strong> = <strong>Ano/Ne</strong>, a <strong>Odstranit rezervace</strong> = <strong>Ano/Ne</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-635">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="33871-636">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="33871-636">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-637">Vyberte položku nabídky <strong>Krátkodobý výdej</strong> v aplikaci skladu při spuštění práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="33871-637">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="33871-638">Do pole <strong>Množství krátkodobého výdeje</strong> zadejte <strong>0</strong> (nula).</span><span class="sxs-lookup"><span data-stu-id="33871-638">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="33871-639">V poli <strong>Důvod</strong> vyberte <strong>Krátkodobý výdej s automaticky opakovaným přidělením</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-639">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-640">Krátkodobé výdeje, které zahrnují automatické opětovné přidělení, nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="33871-640">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="33871-641">Krátkodobé výdeje, které zahrnují automatické opětovné přidělení, nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="33871-641">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="33871-642">Změnit stav zásob</span><span class="sxs-lookup"><span data-stu-id="33871-642">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="33871-643">Tuto akci skladu lze provést z více vstupních bodů.</span><span class="sxs-lookup"><span data-stu-id="33871-643">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="33871-644">Zde zobrazený příklad používá akci **Změna stavu zásob** na stránce **Množství na skladě podle místa**.</span><span class="sxs-lookup"><span data-stu-id="33871-644">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33871-645">Klíčové parametry nastavení</span><span class="sxs-lookup"><span data-stu-id="33871-645">Key setup parameter</span></span></th>
<th><span data-ttu-id="33871-646">Množství dávky je dostupné</span><span class="sxs-lookup"><span data-stu-id="33871-646">Batch quantity is available</span></span></th>
<th><span data-ttu-id="33871-647">Klíčové kroky uživatele</span><span class="sxs-lookup"><span data-stu-id="33871-647">Key user steps</span></span></th>
<th><span data-ttu-id="33871-648">Práce skladu</span><span class="sxs-lookup"><span data-stu-id="33871-648">Warehouse work</span></span></th>
<th><span data-ttu-id="33871-649">Rezervace dávky potvrzené objednávkou</span><span class="sxs-lookup"><span data-stu-id="33871-649">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="33871-650">Na kartě <strong>Sklad</strong> v záznamu <strong>Sklad</strong> je pole <strong>Odstranit rezervace a označení</strong> nastaveno na <strong>Rezervace</strong> nebo <strong>Označení a rezervace</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-650">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="33871-651">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-651">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-652">Vyberte konkrétní umístění.</span><span class="sxs-lookup"><span data-stu-id="33871-652">Select a specific location.</span></span></li>
<li><span data-ttu-id="33871-653">Vyberte řádek s určitou položkou, skladovým místem a registrační značkou (je-li toto umístění řízeno registrační značkou).</span><span class="sxs-lookup"><span data-stu-id="33871-653">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="33871-654">Zvolte <strong>Změna stavu zásob</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-654">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="33871-655">Nastavte pole <strong>Stav zásob</strong> na <strong>Blokování</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-655">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-656">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="33871-656">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="33871-657">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-657">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="33871-658">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-658">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="33871-659">Jsou vytvořeny dvě skladové transakce typu <strong>Změna stavu zásob</strong>, které reprezentují změnu v dimenzi stavu zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-659">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="33871-660">Vytvoří se skladová transakce typu <strong>Blokování zásob</strong> a typu výdeje <strong>Rezervované – fyzicky</strong>, která představuje rezervaci blokovaného množství.</span><span class="sxs-lookup"><span data-stu-id="33871-660">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="33871-661">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-661">No</span></span></td>
<td><span data-ttu-id="33871-662">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-662">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-663">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="33871-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="33871-664">Rezervace je odebrána.</span><span class="sxs-lookup"><span data-stu-id="33871-664">The reservation is removed.</span></span></li>
<li><span data-ttu-id="33871-665">Jsou vytvořeny dvě skladové transakce typu <strong>Změna stavu zásob</strong>, které reprezentují změnu v dimenzi stavu zásob.</span><span class="sxs-lookup"><span data-stu-id="33871-665">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="33871-666">Vytvoří se skladová transakce typu <strong>Blokování zásob</strong> a typu výdeje <strong>Rezervované – fyzicky</strong>, která představuje rezervaci blokovaného množství.</span><span class="sxs-lookup"><span data-stu-id="33871-666">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="33871-667">Na kartě <strong>Sklad</strong> v záznamu <strong>Sklad</strong> je pole <strong>Odstranit rezervace a označení</strong> nastaveno na <strong>Žádná</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-667">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="33871-668">Ano</span><span class="sxs-lookup"><span data-stu-id="33871-668">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="33871-669">Vyberte konkrétní umístění.</span><span class="sxs-lookup"><span data-stu-id="33871-669">Select a specific location.</span></span></li>
<li><span data-ttu-id="33871-670">Vyberte řádek s určitou položkou, skladovým místem a registrační značkou (je-li toto umístění řízeno registrační značkou).</span><span class="sxs-lookup"><span data-stu-id="33871-670">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="33871-671">Zvolte <strong>Změna stavu zásob</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-671">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="33871-672">Nastavte pole <strong>Stav zásob</strong> na <strong>Blokování</strong>.</span><span class="sxs-lookup"><span data-stu-id="33871-672">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="33871-673">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="33871-673">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="33871-674">Množství je znovu rezervováno pro stejnou dávku.</span><span class="sxs-lookup"><span data-stu-id="33871-674">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="33871-675">Systém náhodně přiřadí umístění a registrační značku (pokud je toto umístění řízeno registrační značkou), kde je množství k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33871-675">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33871-676">Ne</span><span class="sxs-lookup"><span data-stu-id="33871-676">No</span></span></td>
<td><span data-ttu-id="33871-677">Viz předchozí řádek.</span><span class="sxs-lookup"><span data-stu-id="33871-677">See the previous row.</span></span></td>
<td><span data-ttu-id="33871-678">Změny stavu zásob nejsou povoleny pro množství, která jsou vyhrazena pro práci.</span><span class="sxs-lookup"><span data-stu-id="33871-678">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="33871-679">Změny stavu zásob nejsou povoleny.</span><span class="sxs-lookup"><span data-stu-id="33871-679">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="33871-680">Omezení</span><span class="sxs-lookup"><span data-stu-id="33871-680">Limitations</span></span>

- <span data-ttu-id="33871-681">Flexibilní funkce rezervace dimenzí na úrovni skladu nepodporuje následující funkce:</span><span class="sxs-lookup"><span data-stu-id="33871-681">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="33871-682">Správa skutečné hmotnosti</span><span class="sxs-lookup"><span data-stu-id="33871-682">Catch weight management</span></span>
    - <span data-ttu-id="33871-683">Záporný fyzický sklad</span><span class="sxs-lookup"><span data-stu-id="33871-683">Physical negative inventory</span></span>
    - <span data-ttu-id="33871-684">Rezervace proti objednané dodávce</span><span class="sxs-lookup"><span data-stu-id="33871-684">Reservation against ordered supply</span></span>
    - <span data-ttu-id="33871-685">Převodní příkazy a výdej surovin</span><span class="sxs-lookup"><span data-stu-id="33871-685">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="33871-686">Pravidlo konsolidace kontejneru pro balení podle jednotky předpisu má omezení.</span><span class="sxs-lookup"><span data-stu-id="33871-686">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="33871-687">V případě rezervací potvrzených objednávkou doporučujeme nepoužívat šablony sestavení kontejnerů, kde je povoleno pole **Zabalit podle jednotky přepisu**.</span><span class="sxs-lookup"><span data-stu-id="33871-687">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="33871-688">V aktuálním návrhu nejsou při vytvoření skladové práce použity směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="33871-688">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="33871-689">Z tohoto důvodu je při kroku vlny vytváření kontejnerů použita pouze nejnižší jednotka ve skupině klasifikace jednotek (skladová jednotka).</span><span class="sxs-lookup"><span data-stu-id="33871-689">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
