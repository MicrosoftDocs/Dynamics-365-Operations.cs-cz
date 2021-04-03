---
title: Blokování zásob
description: Toto téma poskytuje přehled blokování zásob, které je součástí vlastního procesu kontroly kvality v aplikaci Supply Chain Management. Blokování zásob můžete použít pro zabránění zpracování nebo spotřeby položek.
author: perlynne
manager: tfehr
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1d4b006f37904c0ae20691aaa98c75f1d5833b7
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487890"
---
# <a name="inventory-blocking"></a>Blokování zásob

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled blokování zásob, které je součástí vlastního procesu kontroly kvality v aplikaci Supply Chain Management. Blokování zásob můžete použít pro zabránění zpracování nebo spotřeby položek.

Skladové položky lze blokovat následujícími způsoby:

- Ručně
- Vytvořením objednávky kvality.
- Pomocí procesu, který generuje objednávku kvality.
- Použitím blokování stavu zásob

## <a name="blocking-items-manually"></a>Ruční blokování položek

Množství položky je možné blokovat tak, že vytvoříte transakci na stránce **Blokování zásob**. Blokovat lze ručně pouze zboží, které je dostupné na skladě. Při ručním blokování množství je nutné zvážit, zda budou do plánování aktivit zahrnuty očekávané příjmy jako očekávané množství na skladě. Očekávané příjmy jsou blokované položky, u nichž je očekávána dostupnost ve skladu po dokončení kontroly. Očekávané datum můžete spravovat. Standardně je vybrána možnost **Očekávané příjmy** pro položky, které jsou zablokovány pomocí objednávky kvality. Ruční blokování množství lze zrušit odstraněním transakce na stránce **Blokování zásob**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Blokování položek vytvořením objednávky kvality

Je možné zadání položek, které musí být kontrolovány pro vytváření objednávky kvality na stránce **Objednávky kvality**. Při vytváření objednávky kvality je blokováno množství položek, které zadáte. Plán vzorkování, který je spojený s objednávkou kvality, řídí pouze množství položek, které musí být zkontrolovány, nikoli množství, které je blokováno. Bez ohledu na množství, které bude odesláno ke kontrole podle plánu vzorkování, bude blokováno množství položek, které je zadáno v objednávce kvality.

> [!NOTE]
> Hlavní plánování nepodporuje použití funkcí data vypršení platnosti dávky a blokování stavu zásob. To může vést k dvojímu vyloučení množství na skladě, ke kterému může dojít při hlavním plánování. Doporučujeme, abyste při blokování dávek s ukončenou platností spoléhali na kódy dispozice dávky namísto stavu zásob.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blokování položek pomocí procesu, který generuje objednávku kvality

Pokud množství položek uvádí, že je nutné položku zkontrolovat, je množství položek blokováno automaticky. Proto při automatickém generování objednávky kvality řídí plán vzorkování položky, který je spojen s objednávkou kvality, počet blokovaných položek a množství položek, které musí být zkontrolovány. Je-li vybrána možnost **Úplné blokování** na stránce **Vzorkování položek**, celé množství, například řádek nákupní objednávky, bude blokováno při inventuře bez ohledu na množství vzorkování položky.

### <a name="example"></a>Příklad

V následujícím příkladu je generována objednávka kvality po zaúčtování dodacího listu k nákupní objednávce. Na stránce **Přiřazení kvality** jste uvedli, že zaúčtování dodacího listu nákupní objednávky je proces, který aktivuje objednávku kvality.

|Nastavení |Uživatelská akce |Výsledek |
|----|---|---|
| Přiřazení kvality určuje, že při zaúčtování dodacího listu nákupní objednávky musí být vygenerovaná objednávky kvality. Nastavení vzorkování položky objednávky kvality určuje, že musí být zkontrolováno 10 % z počtu řádků nákupní objednávky. Kromě toho vybraná možnost **Úplné blokování** v nastavení položky vzorkování značí, že musí být blokován celý počet řádků nákupní objednávky při inventuře bez ohledu na množství, které je odesláno ke kontrole. | Dodací list bude zaúčtován. | Objednávka kvality bude vygenerována. 10 % z množství položky na nákupní objednávce bude odesláno ke kontrole. Plný počet řádků nákupní objednávky bude blokován. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blokování položek použitím blokování stavu zásob

Můžete určit, jaké stavy zásob jsou stavy blokování, pomocí parametru **Blokování zásob** na stránce **Stavy zásob**.  Stavy zásob nelze použít jako stavy blokování pro výrobní zakázky, prodejní objednávky, převodní příkazy, výstupní transakce nebo integrace projektu. Pro výstupní práci používejte položky, které mají stav zásob „dostupné“. Pokud máte položky se stavem **Zničeno** a použijete u těchto položek hlavní plánování, položky budou považovány za chybějící a sklad se automaticky doplní.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Buďte opatrní při blokování položek, které používají blokování stavu zásob i blokování objednávek kvality

Můžete vytvořit objednávku kvality spojenou se zásobami, která má stav zásob s povoleným parametrem **Blokování zásob**. V takovém případě vygeneruje objednávka kvality kromě záznamu vytvořeného stavem zásob další záznam blokování zásob. Protože blokování zásob objednávky kvality bude mít povoleno parametr **Očekávané příjmy**, vygeneruje se navíc transakce *Objednané zásoby*, která je také blokována svým stavem zásob. Tato kombinace může vést k potížím v chápání významu generovaných transakcí zásob, protože se bude zdát, že celkové blokované množství přesahuje celkové množství na skladě. Prozkoumejme transakce na příkladu příjmu 10 kusů položky A0001 s objednávkou kvality vygenerovanou pro vzorek 1 kusu. Chování bude také záviset na tom, zda je zapnuta možnost **Rezervovat objednané položky** ve stránce **Parametry modulu Řízení zásob a skladu**.

>[!NOTE]
>Pokud používáte blokování stavu zásob a objednávky kvality společně, důrazně doporučujeme mít zapnutou možnost **Rezervovat objednané položky**.

### <a name="example-with-reserve-ordered-items-enabled"></a>Příklad se zapnutou možností „Rezervovat objednané položky“

Když je zapnuta možnost **Rezervovat objednané položky**, všechny transakce blokující zásoby budou mít stav buď *Rezervované – fyzicky*, nebo *Rezervované – objedn.*.

| Odkaz na skladovou transakci | Příjem | Výdej | Množství | Lokalita | Sklad | Stav skladu | Skladové místo | Registrační značka | Komentář |
|---|---|---|---|---|---|---|---|---|---|
| Nákupní objednávka | Koupeno | | 10 kusů | 2 | 24 | Blokování | RECV | receiptLp1 | | 
| Blokování zásob | | Rezervované – fyzicky | -9 kusů | 2 | 24 | Blokování | | | Transakce vygenerovaná blokováním stavu zásob |
| Blokování zásob | | Rezervované – fyzicky | -1 kus | 2 | 24 | Blokování | RECV | receiptLp1 | Transakce generovaná blokováním vzorkování objednávky kvality |
| Blokování zásob | Objednáno | | 1 kus | 2 | 24 | Blokování | RECV | receiptLp1 | Očekávané příjmy z blokování vzorkování objednávky kvality |
| Blokování zásob | | Rezervované – objedn. | 1 kus | 2 | 24 | Blokování | | | Transakce vygenerovaná blokováním stavu zásob

### <a name="example-with-reserve-ordered-items-disabled"></a>Příklad s vypnutou možností „Rezervovat objednané položky“

Když je možnost **Rezervovat objednané položky** vypnuta, očekávané příjmy nelze rezervovat, protože jsou ve stavu *Objednáno*, takže některé blokování zůstane ve stavu *Na objednávce*.

| Odkaz na skladovou transakci | Příjem | Výdej | Množství | Lokalita | Sklad | Stav zásob | Skladové místo | Registrační značka | Komentář |
|---|---|---|---|---|---|---|---|---|---|
| Nákupní objednávka | Koupeno | | 10 kusů | 2 | 24 | Blokování | RECV | receiptLp1 | |
| Blokování zásob | | Rezervované – fyzicky | -9 kusů | 2 | 24 | Blokování | | | Transakce vygenerovaná blokováním stavu zásob |
| Blokování zásob | | Rezervované – fyzicky | -1 kus | 2 | 24 | Blokování | RECV | receiptLp1 | Transakce generovaná blokováním vzorkování objednávky kvality |
| Blokování zásob | Objednáno | | 1 kus | 2 | 24 | Blokování | RECV | receiptLp1 | Očekávané příjmy z blokování vzorkování objednávky kvality |
| Blokování zásob | | Na objednávce | 1 kus | 2 | 24 | Blokování | RECV | receiptLp1 | Transakce vygenerovaná blokováním stavu zásob

Všimněte si rozdílu ve stavu transakce a dimenzích mezi těmito dvěma případy. Z tohoto důvodu doporučujeme zapnout možnost **Rezervovat objednané položky**.

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>Další prostředky

[Vytvoření a správa blokování zásob](tasks/create-maintain-inventory-blocking.md)

[Procesy správy kvality](quality-management-processes.md)

[Kontrola kvality zboží](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]