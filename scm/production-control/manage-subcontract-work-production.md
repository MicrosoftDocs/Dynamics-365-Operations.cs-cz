---
title: "Správa subdodavatelské práce při výrobě"
description: "Toto téma vysvětluje, jak jsou subdodavatelské operace spravovány v aplikaci Microsoft Dynamics 365 for Operations. Jinými slovy vysvětluje, jak dodavatel spravuje výrobní operace přiřazené prostředku."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 4b5830d50297598863b8a7a7611e11a29afeab63
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Správa subdodavatelské práce při výrobě

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak jsou subdodavatelské operace spravovány v aplikaci Microsoft Dynamics 365 for Operations. Jinými slovy vysvětluje, jak dodavatel spravuje výrobní operace přiřazené prostředku.

Ve [výrobních procesech](production-process-overview.md) mohou práci provádět zdroje, které jsou vlastněné nebo spravované dodavateli. Prostředky dodavatele se používají k vyrovnání pravidelné nadměrné poptávky, která překračuje dostupnou kapacitu vlastních prostředků společnosti. Dodavatel může být také schopen nabídnout konkrétní [schopnosti prostředku](resource-capabilities.md)nebo prostředky za nižší cenu.  

V závislosti na prostředcích dodavatele použitých ve výrobním procesu [postupu](routes-operations.md) často existují další logistické požadavky, protože materiál a polotovary musí nejprve přepraveny do sídla dodavatele. Pak musí být výsledek operace subdodávek přepraven buď do umístění, které je přiřazeno k další operaci, nebo do skladu hotových výrobků.  

Pokud jsou použity subdodávky operací nebo činnosti, mají vliv na všechny fáze operací, z definice operací, které jsou vyžadovány ve výrobě, ocenění, prognózování, plánování a vytvoření harmonogramu pro správu logistiky materiálů, polotovarů a hotových výrobků. Nakonec tyto prostředky vyžadují své vlastní procesy pro účetnictví a řízení nákladů.  

Pro vnitřní zdroje je pro období typicky přidělena pevná sazba nákladů. Naopak náklady na nasmlouvaný subodavatelský prostředek vycházejí z nákupní ceny souvisejících služeb. Služba je definována jako jiný produkt a používá se k řízení zásobování veřejných zakázek a nákupních procesů pro dané operace subdodávek.  

V současné době v aplikaci Microsoft Dynamics 365 for Operations neexistuje žádný explicitní koncept polotovarů. U výrobních zakázek, které vyžadují více než jednu operaci pro účely transformace surovin na hotový výrobek, je hotové zboží účtováno zpět do zásob pouze u poslední operace. Rozpracované výrobky, které vyvolávají dřívější operace jsou zaúčtovány nedokončené výroby (NV), ale nejsou zaúčtovány nebo sledovány ve skladu. Přestože postupy a kusovníky (BOM) můžete rozdělit na několik menších jednotek, tento přístup zvyšuje počet produktů, kusovníky a postupy, které musí být spravovány.  

Existují dvě metody pro modelování subdodavatelské práce pro výrobní činnosti. Tyto metody se liší ve způsobu, jakým lze modelovat subdodávky procesu, ve způsobu, jakým jsou rozpracované výrobky zastoupeny v procesu a ve způsobu řízení nákladů.

-   Subdodávky operací postupu ve výrobních zakázkách nebo dávkových objednávkách
    -   Servisní produkt musí být v zásobách a musí být součástí kusovníku.
    -   Tato metoda podporuje první, první ze skladu (FIFO) nebo standardní náklady.
    -   Polotovary jsou představovány produktem služby v procesu.
    -   Řízení nákladů přiděluje náklady, které jsou přidruženy k práci subdodavatele na materiálové náklady.
-   Subdodávky aktivity výrobního toku v toku štíhlé výroby
    -   Služba je služba neuskladněného produktu a není součástí tohoto kusovníku.
    -   Tato metoda používá nákupní smlouvy jako servisní smlouvy.
    -   Tato metoda používá zpětné účtování nákladů.
    -   Tato metoda umožňuje souhrnné a asynchronní zásobování. (Tok materiálu je nezávislý na procesu zadávání veřejných zakázek).
    -   Řízení nákladů přiděluje subdodavatelskou práci ve vlastním bloku rozdělení nákladů.

## <a name="subcontracting-of-route-operations"></a>Subdodávky operací postupu
Abyste mohli používat operace postupu pro výrobu nebo dávkové objednávky subdodávky, musí být servisní produkt, který se používá pro zadávání zakázek na služby, být definován jako produkt typu **Služba**. Kromě toho musí mít skupinu modelů zboží, která má možnost **Výrobek na skladě** v části **Zásada zásob** nastavenou na **Ano**. Tato možnost definuje, zda je produkt účtován jako příjem zásob v produktu (**Výrobek na skladě** = **Ano**), nebo zda je produkt zanesen do výdajů na účtu zisků a ztrát (**výrobek na skladě** = **Ne**). Ačkoli se toto chování může jevit jako sporné, je založeno na skutečnosti, že pouze produkty, u kterých platí tyto zásady, vytvoří skladové transakce, které lze použít v řízení nákladů pro výpočet plánovaných nákladů a určení skutečných nákladů po ukončení výrobní zakázky.  

Aby byla služba zohledněna při výpočtu plánování a nákladů, musí být přidána ke kusovníku. Řádek kusovníku musí být typu **Dodavatel** typu a musí být přidělen k operaci postupu, ke které je přidělená služba. Tato operace postupu musí mít prostředek výpočtu nákladů a požadavek na zdroj, který odkazuje na typ **dodavatele** typu, který se připojuje k operaci a související službě odpovídajícího účtu dodavatele.  

Při použití této konfigurace je vytvořena nákupní objednávka produktu související služby, založené na odhadu výrobní zakázky. Objednávka služby slouží jako kotva pro operace subdodávek. Subdodavatelské práce lze spravovat prostřednictvím stránky seznamu **Subdodávka prací** v řízení výroby. Subdodavatelské práce slouží k dodání surovin a následně polotovaru dodavateli v rámci přípravy operaci. Také slouží k příjmu výsledného produktu subdodavatelské operace při doručení položky, kde je servisní produkt používán k identifikaci příchodu polotovaru. Při přijetí řádku nákupní objednávky je aktualizována výrobní operace jako dokončená.  

Výrobní zakázka může mít mnoho operací a každou operaci lze přidělit jinému dodavateli. Proto může koncový výrobní příkaz aktivovat více nákupních objednávek.

## <a name="subcontracting-of-production-flow-activities"></a>Subdodávky aktivity výrobního toku
Řešení [lean manufacturing](lean-manufacturing-overview.md)modeluje subdodavatelskou práci jako službu, která souvisí s aktivitou výrobního toku [výrobní tok](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (Téma Průvodce záznamem úloh). Proto je tento typ subdodávky také označován jako [subdodávky podle aktivity](activity-based-subcontracting.md) Zavádíme speciální typ nákladové skupiny s názvem **Přímý outsourcing** a subdodavatelské služby nejsou součástí kusovníku hotového zboží. Při použití lean manufacturing jsou všechny aktivity definovány kanbany, které lze propojit s jednou nebo více aktivitami výrobního toku. Toto vysvětlení zatím zní jako popis výrobních zakázek. Zatímco výrobní zakázky musí vždy končit hotovým výrobkem, můžete vytvořit kanbany pro dodávku polotovarů. Není nutné zavést novou úroveň produktu a kusovníku.  

Kanbanová pravidla mohou být velmi dynamická, můžete modelovat různé varianty zásobování pro stejný produkt ve výrobním toku. Při použití štíhlých subdodávek jsou tok materiálu a finanční toku striktně odděleny. Všechny toky materiálu jsou reprezentovány kanbanovými aktivitami. Nákupní objednávky pro produkty služby a zaúčtování příjmu těchto služeb lze automatizovat na základě stavu kanbanových úloh ve výrobním toku. Kanbanové úlohy můžete spustit a dokončit ještě dříve, než jsou vytvořeny nákupní objednávky. Doklady o subdodávce mohou být agregovány (nákupní objednávka a nákupní příjemka služby) podle období a služby. Proto počet nákupních dokladů a řádků může být uchováván v malém množství i v často opakovaných operacích, kde dodavatelé poskytují subdodavatelské služby v toku jednoho kusu.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modelování subdodávek ve výrobním toku

V [štíhlém výrobním toku](lean-manufacturing-modeling-lean-organization.md) lze aktivitu procesu definovat jako subdodávku při přidělení jedné pracovní buňce (skupině zdrojů), která má jeden dodavatelský zdroj. Pokud je subdodávána pracovní buňka, související procesní aktivity musí být spojeny s nákupním řádkem aktivní smlouvy obsahující předmět služby a cenu za službu. Servisní smlouva aktivity definuje také poměr výpočtu mezi množstvím produktu kanbanové úlohy a výsledným množstvím služeb. Můžete určit, zda bude množství služby vypočítáno na základě počtu úloh, dobrého množství produktu, které je vykázáno u práce nebo celkového množství produktu (toto množství zahrnuje vyřazené produkty).  

Aktivity přenosu lze také definovat jako subdodávky. Tato definice se objevuje implicitně když vyberete odpovědnou stranu pro expedici v aktivitě přenosu. Pokud vyberete **dopravce** nebo **příjemce** a zdrojový nebo cílový sklad spravuje dodavatel, je tato aktivita považována za subdodávku. Pokud vyberete **dopravce**, aktivita je vždy zadána jako subdodavatelská. Jako u aktivit subdodavatelského procesu musí být subdodavatelská aktivita přenosu připojena k servisní smlouvě před aktivací výrobního toku.

### <a name="backflush-costing"></a>Zpětné účtování nákladů

Nákladové účetnictví subdodavatelské práce je plně integrováno do řešení výpočtu nákladů pro lean manufacturing (zpětné účtování nákladů). Při zaúčtování příjemky nákupní objednávky služby nebo při fakturaci budou náklady na služby přiděleny výrobnímu toku. Pro zpětné účtování nákladů se vypočítá rozptyl subdodavatelské služby započtením bloku subdodávek standardních nákladů přijatých produktů proti skutečným přijatým a fakturovaným množstvím služby.

## <a name="material-supply-for-subcontracted-operations"></a>Dodávka materiálu pro operace subdodávek
Polotovary a ostatní související materiály musí být převedeny do umístění, kde je práce prováděna fyzicky. Při použití operací a aktivit subdodávek tento převod často souvisí s další přepravou na web provozovaný dodavatelem. Přidělením materiálu v kusovníku operacím subdodávek deklarujete, že materiál musí být ve fázi na vstupním místě skupiny prostředků přiděleného zdroje. Hlavní plánování nebo štíhlé doplnění pak zprostředkovává doplněné materiálu do daného umístění.  

Pro modelování zásob, které jsou umístěny na webu dodavatele, je nejlepší praxe v odvětví definovat sklad řízený dodavatelem. Snadno můžete definovat sklad řízený dodavatelem vytvořením nového skladu a přiřazením účtu dodavatele. Pokud chcete zdokumentovat, že tento materiál musí být přemístěn dodavateli před provedením operace, měli byste přidělit sklad spravovaný dodavatelem do vstupního skladu skupiny prostředků obsahující prostředek.  

K doplnění materiálu v tomto skladu, můžete použít více strategií:

-   Převodní příkazy
-   Převést deníky
-   Kanbany odběru
-   Přímý nákup v umístění dodavatele

Polotovary jsou výjimkou z tohoto pravidla. K přenosu polotovarů jste omezeni na tyto možnosti:

-   Pokud jde o výrobu a dávkové objednávky, rozpracované výrobky mohou být přenášeny pouze logicky pomocí deníku výdejek ze stránky se seznamem **subdodávka prací**. Tento deník vytvoří dokument dodacího listu, který lze použít k přenosu polotovarů a surovin dodavateli.
-   Pro operace subdodávek ve výrobních tocích je převod polotovarů doložen příjmem odvolání nebo výrobních kanbanů v místě dodavatele. Pokud chcete modelovat explicitní aktivitu převodu, můžete ukončit výrobní kanban s další aktivitou přenosu.

**Poznámka:** Postup výroby pro jednu výrobní zakázku nemůže přesahovat více míst. Toto pravidlo platí také pro práci subdodavatele. Proto sklady představující umístění materiálu spravovaného dodavatelem musí být definovány ve stejné síti jako interní zdroje, které jsou použity v postupu. Přestože výrobní toky mohou zahrnovat více pracovišť, nemohou převádět polotovary z jednoho pracoviště na jiné, protože operace implikuje změnu kontextu nákladů.  

Obvykle jsou výstupní sklad a umístění subdodavatelské skupiny prostředků skupiny přímo přiděleny skladu a umístění dalšího kroku operace v postupu nebo výrobním toku. Toto nastavení pomáhá snížit množství vykazování úloh, které se objeví, nebo na počtu dalších operací přenosu, které musí být modelovány.




