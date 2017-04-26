---
title: "Subdodavatelské práce při výrobě spravovat"
description: "Toto téma vysvětluje, jak subdodavatelské operace jsou spravovány v 365 Microsoft Dynamics pro operace. Jinými slovy vysvětluje způsob správy výrobních operací, které jsou přiděleny k prostředku podle dodavatele."
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
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Subdodavatelské práce při výrobě spravovat

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak subdodavatelské operace jsou spravovány v 365 Microsoft Dynamics pro operace. Jinými slovy vysvětluje způsob správy výrobních operací, které jsou přiděleny k prostředku podle dodavatele.

V [výrobních procesů](production-process-overview.md), zdroje, které jsou vlastněné nebo spravované dodavatelů lze provést práce. Prostředky dodavatele se obvykle používají k úrovni pravidelné nadměrná poptávka, která překročí dostupnou kapacitu společnosti vlastní prostředky. Dodavatel může být také nabídnout konkrétní [schopnosti prostředku](resource-capabilities.md)nebo zdroje za nižší cenu.  

V závislosti na dodavatele zdroje použité ve výrobním procesu [postupu](routes-operations.md) má často další logistické, protože materiál a polotovary musí nejprve přepravovat na webu dodavatele. Výsledek operace subdodávek pak musí být přepravovány buď do umístění, které je přiřazen k další operaci nebo do skladu hotových výrobků.  

Pokud jsou použity subdodávky operací nebo činnosti, mají vliv na všechny fáze operace z definice operací, které jsou vyžadovány v produkci, ocenění, Prognózování, plánování a plánování pro správu logistiky materiálu, polotovarů a hotových výrobků. Nakonec tyto prostředky vyžadují své vlastní procesy pro účetnictví a řízení nákladů.  

Vnitřní zdroje obvykle po dobu přidělena Pevná nákladová sazba. Naopak náklady na subdodavatele zdroje podle nákupní ceny souvisejících služeb. Služba je definována jako jiný produkt a se používá jednotka zadávání veřejných zakázek a nákupní procesy pro dané operace subdodávek.  

V současné době neexistuje žádný explicitní koncept polotovarů v 365 Microsoft Dynamics pro operace. Výrobní zakázky, která vyžaduje více než jednu operaci pro transformaci suroviny do hotového výrobku hotového zboží účtována zpět do zásob pouze u poslední operace. Rozpracované výrobky, které vyvolávají dřívější operace jsou zaúčtovány nedokončené výroby (NV), ale nejsou zaúčtovány nebo sledovány ve skladu. Přestože postupy a kusovníky (BOM) můžete rozdělit na několik menších jednotek, tento přístup zvyšuje počet produktů, kusovníky a postupy, které musí být spravovány.  

Existují dvě metody pro modelování subdodavatelské práce pro výrobní činnosti. Tyto metody se liší způsobem, že subdodávky procesu lze modelovat, způsobu, jakým rozpracované výrobky jsou zastoupeny v procesu a je spravována tak, aby řízení nákladů.

-   Subdodávky operací postupu výrobní zakázky nebo dávkové objednávky
    -   Produkt service musí být produkt skladem a musí být součástí tohoto Kusovníku.
    -   Tato metoda podporuje první, první ze skladu (FIFO) nebo standardní náklady.
    -   Polotovary jsou představovány služby produktu v procesu.
    -   Řízení nákladů přidělí náklady, které jsou přidruženy práce subdodavatele na materiálové náklady.
-   Subdodávky aktivity výrobního toku v toku štíhlé výroby
    -   Služba je služba skladě produktu a není součástí tohoto Kusovníku.
    -   Tato metoda používá nákupní smlouvy jako servisní smlouvy.
    -   Tato metoda používá zpětné účtování nákladů.
    -   Tato metoda umožňuje pro zásobování souhrnné a asynchronní. (Toku materiálu je nezávisle na procesu zadávání veřejných zakázek).
    -   Řízení nákladů přiděluje práce subdodavatele v bloku rozdělení své vlastní náklady.

## <a name="subcontracting-of-route-operations"></a>Subdodávky operací postupu
Použití operace postupu pro výrobu nebo dávkové objednávky subdodávky, servisní produkt, který se používá pro zadávání zakázek na služby musí být definována jako součin **služby** typu. Kromě toho musí mít skupinu modelů zboží, který má **výrobek na skladě** možnost ve skupinovém rámečku **zásob zásad** nastavena na **Ano**. Tato možnost určuje, zda je produkt účtována jako skladové příjemky produktu (**výrobek na skladě** = **Ano**), nebo zda je produkt zanesen do výdajů na účtu zisků a ztrát (**výrobek na skladě** = **č**). Ačkoli toto chování může jevit jako sporné, je založena na skutečnosti, že pouze produkty, u kterých je tato zásada, vytvoří skladové transakce, které lze použít v řízení nákladů pro výpočet plánovaných nákladů a určení skutečné náklady po ukončení výrobní zakázky.  

Mají být zohledněny při výpočtu plánování a nákladů, musí být služba přidána ke Kusovníku. Řádek Kusovníku musí být **dodavatele** typu a musí být přidělena, je služba přidělena k operaci postupu. Tato operace postupu musí mít prostředek výpočtu nákladů a přejděte na zdroj požadavek na prostředek **dodavatele** typu, který se připojuje k odpovídající účet dodavatele operace a související služby.  

Při použití této konfigurace je vytvořena nákupní objednávka produktu související služby, založené na odhadu výrobní zakázky. Objednávka služby slouží jako kotva pro operace subdodávek. Subdodavatelské práce lze spravovat prostřednictvím **subdodávka prací** seznam stránek v řízení výroby. Subdodavatelské práce slouží k dodání surovin a následně polotovar dodavatele v rámci přípravy operaci. Také slouží k příjmu získaného produktu subdodavatelské operace v doručení položky, kde produkt service se používá k identifikaci příchodem polotovaru. Přijetí řádku nákupní objednávky je aktualizován výrobní operaci jako dokončenou.  

Výrobní zakázka, může mít mnoho operací a každé operace mohou být přiděleny jinému dodavateli. Konec konec výrobní objednávky, proto mohou být aktivována více nákupních objednávek.

## <a name="subcontracting-of-production-flow-activities"></a>Subdodávky aktivity výrobního toku
[Štíhlé výroby](lean-manufacturing-overview.md)řešení modely subdodavatelské práce jako služba vztahující se k činnosti [výrobní tok](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (téma Průvodce úkolu). Proto tento typ subdodávky jsou také označovány jako [podle činností subdodavatelů.](activity-based-subcontracting.md) Typ skupiny nákladů speciální **přímý outsourcing**, byly zavedeny, a subdodavatelské služby nejsou součástí Kusovníku dokončené zboží. Při použití lean manufacturing, všechny aktivity jsou definovány kanbany, které lze propojit s jedním nebo více aktivity výrobního toku. Toto vysvětlení, pokud zvuky stejně jako popis výrobní zakázky. Že výrobní zakázky musí vždy končit konečného výrobku, je vytvořit kanbany dodávat polotovar. Není nutné zavést nový produkt a úroveň Kusovníku.  

Kanbanová pravidla mohou být velmi dynamický, můžete různé varianty zásobování pro stejný produkt modelu výrobního toku. Při použití štíhlých subdodávky toku materiálu a finančního toku jsou striktně odděleny. Všechny toku materiálu je reprezentován kanbanových aktivit. Nákupní objednávky pro produkty, služby a zaúčtování příjmu těchto služeb lze automatizovat, na základě stavu kanbanové úlohy ve výrobním toku. Kanbanové úlohy můžete spustit a dokončit ještě dříve, než jsou vytvořeny nákupní objednávky. Období a služby může být agregovaný dokumenty subdodávky (nákupní objednávky a nákupní příjemce služby). Proto počet nákupních dokladech a řádcích může být uchováván malé i ve vysoce opakované operace, které dodavatelé poskytují subdodavatelské služby v toku jednoho kusu.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Subdodávky ve výrobním toku modelování

V [štíhlé výrobní tok](lean-manufacturing-modeling-lean-organization.md), aktivitu procesu lze definovat jako subdodávka při přidělení na jediného dodavatele zdroj pracovní buňka (skupina prostředků). Pokud je zadána pracovní buňka, činnosti související proces musí být spojeny s aktivní nákupní řádek smlouvy obsahující předmět servisu a cenu za službu. Servisní smlouvy aktivity definuje také výpočet poměr mezi množstvím produktu kanbanové úlohy a výsledné množství služeb. Můžete určit, zda služba množství se vypočítá na základě počtu úloh, množství dobré produktu je hlášena u projektů nebo množství celkového produktu (toto množství zahrnuje vyřazené produkty).  

Na činnost přenosu lze také definovat jako subdodávka. Tato definice dojde implicitně vybrat odpovědná strana pro expedici do této aktivity přenosu. Pokud vyberete **dopravce** nebo **příjemce**, pokud zdrojový nebo cílový sklad sklad dodavatele spravované, činnost je považována za zadána. Pokud vyberete **dopravce**, aktivity je vždy zadána. Jako subdodavatele proces aktivity aktivitu subdodávek přenosu musí být připojen k servisní smlouvě před aktivací výrobního toku.

### <a name="backflush-costing"></a>Zpětné účtování nákladů

Subdodavatelské práce nákladového účetnictví je zcela integrována do nákladů řešení lean manufacturing (zpětné účtování nákladů). Při zaúčtování nákupní objednávky příjemce služby nebo při fakturaci, náklady na služby bude přidělena výrobní tok. Pro zpětné účtování nákladů, se vypočítá rozptyl subdodavatelské služby započtením subdodávky blok standardních nákladů přijatých produktů proti skutečné služby přijaté a Fakturované množství.

## <a name="material-supply-for-subcontracted-operations"></a>Dodávek materiálu pro operace subdodávek
Polotovary a ostatních souvisejících materiálů musí být přepraveno do umístění, kde je práce prováděna fyzicky. Při použití operace subdodávek a činnosti tento převod často souvisí další přepravy na web dodavatele provozována. Přidělením materiál v Kusovníku pro operace subdodávek prohlásit, že materiál musí být připravené na vstupní místo skupiny zdrojů přidělené zdroje. Hlavní plánování nebo doplnění štíhlé pak ustanovení materiálu do daného umístění.  

Pro model zásob, která je umístěna na webu dodavatele, je nejlepší praxe v odvětví definovat spravované dodavatelem skladu. Snadno můžete definovat sklad dodavatele spravovat vytvořením nového skladu a přiřazení účtu dodavatele. Dokumentovat tento materiál musí být přemístěno do dodavatele před provedením operace, přidělovat sklad dodavatele spravované vstupní sklad skupinu prostředků obsahující prostředek.  

K doplnění materiálu v tomto skladu, můžete použít více strategií:

-   Převodní příkazy
-   Převést deníky
-   Kanbany
-   Přímý nákup na umístění dodavatele

Polotovary jsou výjimkou z tohoto pravidla. K přenosu polotovarů, jsi omezen na tyto možnosti:

-   Pro výrobu a dávkové objednávky rozpracované výrobky mohou být přenášeny pouze logicky pomocí deníku výdejek z **subdodávka prací** stránku seznamu. Tento deník vytvoříte dodací list dokumentu, který lze použít k přenosu polotovary a suroviny na dodavatele.
-   Pro operace subdodávek ve výrobních toků převod polotovarů je doložena obdržení odvolání nebo výrobní kanbany v místě dodavatele. Pro model explicitní převod činnost, můžete ukončit výrobní kanban s aktivitou další přenos.

**Poznámka:** postupu výroby pro jednu výrobní zakázku nelze mezi více serverů. Toto pravidlo platí také pro práci subdodavatele. Proto sklady představující umístění musí být definovány ve stejné síti jako vnitřní zdroje, které jsou použity v postupu spravované dodavatele materiálu. Přestože výrobní toky lze mezi servery, jejich nelze dopravní polotovarů z jednoho webu na jiný, protože operace nemění kontextu náklady.  

Obvykle výstupní sklad a umístění subdodavatelů prostředku skupiny jsou přímo přiděleny skladu a umístění další krok operace v postupu nebo výrobní tok. Toto nastavení pomáhá snížit množství úloha oznámení, že v takovém nebo číslo další přenos operací, které musí být modelována.




