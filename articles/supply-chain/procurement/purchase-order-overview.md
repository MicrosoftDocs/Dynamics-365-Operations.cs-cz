---
title: "Přehled nákupních objednávek"
description: "Tento článek poskytuje obecné informace o nákupních objednávkách a odkazy na další články, které se týkají různých fází, kterými prochází nákupní objednávka."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d01ef1c496c7c79795d9d740ee755e84434dfdf1
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="purchase-order-overview"></a>Přehled nákupních objednávek

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Tento článek poskytuje obecné informace o nákupních objednávkách a odkazy na další články, které se týkají různých fází, kterými prochází nákupní objednávka.

Nákupní objednávka je dokument, který představuje dohodu s dodavatelem k nákupu zboží nebo služeb. Dokument také pomáhá udržet přehled o příjemkách produktu, které byly vytvořeny pro objednávku, a později o účtování faktur dodavatele, které dodavatel fakturuje pro objednávku.  

Stránka **Nákupní objednávky** obsahuje přehled dostupných objednávek a umožňuje tyto objednávky měnit. Po otevření nákupní objednávky můžete vybrat zobrazení **Záhlaví**, které obsahuje informace, které jsou určeny pouze jednou pro každou nákupní objednávku, jako jsou podrobnosti o dodavateli. Případně můžete vybrat zobrazení **Řádky**, kde můžete měnit řádky objednávky. Obvykle budete přepínat mezi těmito dvěma zobrazeními při změnách nákupních objednávek. Poplatky nejsou uvedeny přímo na stránce **Nákupní objednávky**, ale jsou přístupné prostřednictvím nabídek v záhlaví a na řádkách objednávky.  

Existuje mnoho sestav, kde můžete zobrazit informace o nákupních objednávkách, příjemkách produktu a fakturách dodavatele. Tyto zprávy jsou součástí modulů **Zásobování a zdroje** a **Závazky**.  

Pracovní prostory **Příprava nákupní objednávky** a **Příjem a zpracování nákupní objednávky** umožňují zobrazit seznamy nákupních objednávek v různých stavech, do kterých dospěly. Poskytují také souhrn akcí, které je třeba provést. Pracovní prostor **Příprava nákupní objednávky** se zaměřuje na vytváření nákupních objednávek a jejich přezkoumání, zpracování objednávky prostřednictvím schválení a potvrzení u dodavatele. Pracovní prostor **Příjemka a zpracování nákupní objednávky** se zaměřuje na zpracování příjmu zboží nebo služeb proti nákupním objednávkám. Obsahuje seznamy, které umožňují pohled na příjmy, které jsou zpožděné nebo které budou brzy určené pro dodání dodavatelem. Tyto pracovní prostory nejsou používány k souvisejícím činnostem pro příjem, které jsou prováděny ve skladu. Tyto činnosti jsou prováděny prostřednictvím stránek v modulu **Řízení zásob** a **Řízení skladu**. Zpracování faktur dodavatele by mělo být provedeno pomocí pracovního prostoru **Záznamy faktury dodavatele**, a platby by se měly provést pomocí pracovního prostoru **Platby dodavatele**.  

Následující články poskytují přehled o různých fázích, kterými prochází nákupní objednávky:

-   [Vytvoření nákupní objednávky](purchase-order-creation.md)
-   [Potvrzení a odmítnutí nákupní objednávky](purchase-order-approval-confirmation.md)
-   [Příjem produktů proti nákupním objednávkám](product-receipt-against-purchase-orders.md)
-   [Přehled faktur dodavatele](../../financials/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Typy nákupních objednávek
Existují tři typy nákupních objednávek: Při vytváření nákupní objednávky je nutné zadat její typ. Výchozí typ pro nové objednávky můžete nastavit na stránce **Parametry modulu Zásobování a zdroje**.

| Typ nákupní objednávky        | Popis                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Deník        | Tento typ slouží k vytvoření návrhu objednávky. Tento typ nemá vliv na množství zásob nebo generování skladových transakcí. Řádky deníku nákupní objednávky nejsou obsaženy v hlavním plánování.                                                                                                       |
| Nákupní objednávka | Tento typ slouží k vytvoření nákupních objednávek při potvrzení objednávky u dodavatele, a při zpracování objednávek prostřednictvím příjmu a fakturace před uhrazením platby dodavateli. Tento typ nákupní objednávky je nejčastější.                                                                          |
| Vratka | Tento typ použije, když se dodavateli vrací zboží. Tento typ objednávky vyžaduje zadání číslo RMA (schválení vrácených materiálů), které vám poskytne dodavatel. Číslo RMA určíte na kartě **Obecné** u nákupní objednávky. Řádky objednávky musí mít záporné množství. |

## <a name="purchase-order-statuses"></a>Stavy nákupní objednávky
Nákupní objednávky obsahují několik polí se stavem, které označují průběh objednávky. Všechna tato pole jsou zobrazena v zobrazení **Záhlaví** objednávky a několik z nich je také zobrazeno v mřížce představující přehled všech objednávek. Pole **Stav** zobrazuje stav množství na objednávce. K dispozici jsou následující hodnoty:

-   **Otevřená objednávka** – objednávky byly vytvořeny a množství je v pořádku.
-   **Přijaté** – některé množství bylo přijato, ale nebylo dosud fakturováno.
-   **Fakturované** – bylo fakturováno celé množství na objednávce. **Poznámka:** Pokud objednávka byla *částečně* fakturována, není vhodný stav **Přijato** ani **Fakturováno**. Proto má objednávka stále stav **Otevřená objednávka**.
-   **Zrušeno** – objednávka byla potvrzena, ale později zrušena. Proto tento stav znamená, že již neexistují žádná otevřená množství na objednávce.

Pole **Stav dokumentu** umožňuje rychle zkontrolovat průběh objednávky, pokud jde o dokumenty, které byly zpracovány. Zobrazuje se zde stav posledního dokumentu, který byl dokončen pro objednávku. K dispozici jsou následující hodnoty:

-   **Žádný** – žádný dokument nebyl dosud pro objednávku zpracován.
-   **Nákupní žádanka** – byl vygenerován nákupní dotaz a objednávka čeká na zpětnou vazbu od dodavatele.
-   **Nákupní objednávka** – bylo zpracováno potvrzení objednávky.
-   **Příjemka produktu** – příjemka produktu u objednávky byla zpracována.
-   **Faktura** – faktura byla zaúčtována u objednávky.

Pole **Stav schválení** se používá, když nákupní objednávka prochází procesem kontroly nebo pracovním postupem. K dispozici jsou následující hodnoty:

-   **Návrh**, **Probíhá kontrola** a **Odmítnuto** – tyto stavy jsou použity pouze v případě, že se pro nákupní objednávku používá pracovní postup schválení.
-   **Schváleno** – tento stav je přiřazen k objednávkám, které mají dokončen pracovní postup schválení. Objednávky vytvořené bez použití pracovního postupu schválení obdrží stav **Schváleno** okamžitě.
-   **Na externí kontrole** – tento stav se používá v případech, kde je nákupní žádanka odeslána dodavateli, aby dodavatel mohl potvrdit podmínky nákupní objednávky. Tento stav se také používá v procesu, který je spouštěn akcí **Žádost o potvrzení**. Pro tento proces je dodavatel požádán o potvrzení podmínek nákupní objednávky připojením do vašeho systému a zaregistrováním toho, zda je objednávka potvrzena nebo odmítnuta.
-   **Potvrzeno** – tento stav je přiřazen poté, co objednávka byla potvrzena. Tento stav je obvykle poslední stav schválení přiřazený k objednávce.


<a name="additional-resources"></a>Další zdroje
--------

[Vytvoření nákupní objednávky](purchase-order-creation.md)

[Potvrzení a odmítnutí nákupní objednávky](purchase-order-approval-confirmation.md)

[Příjem produktů proti nákupním objednávkám](product-receipt-against-purchase-orders.md)

[Přehled faktur dodavatele](../../financials/accounts-payable/vendor-invoices-overview.md)




