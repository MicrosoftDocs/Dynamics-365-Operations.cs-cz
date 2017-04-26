---
title: "Podle činností subdodavatelů"
description: "Toto téma popisuje podrobně, jak používat subdodavatelských činností ve výrobním toku pro lean manufacturing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Podle činností subdodavatelů

[!include[banner](../includes/banner.md)]


Toto téma popisuje podrobně, jak používat subdodavatelských činností ve výrobním toku pro lean manufacturing.

V Microsoft Dynamics 365 pro operace, existují dva přístupy pro subdodávky: výrobní zakázky a štíhlé výroby. V metodě lean manufacturing subdodavatelské práce je modelována jako službu, která souvisí s aktivity výrobního toku. Zvláštní typ typ nákladové skupiny s názvem **přímý outsourcing** byl zaveden, a subdodavatelské služby jsou již součástí kusovníku (BOM). Subdodavatelské práce nákladového účetnictví je plně integrována do ocenění řešení pro lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Výrobní toky, které se týkají subdodavatelů
Při činnosti jsou předmětem subdodávky, nezmění se základním principem výrobního toku. Materiál stále toky mezi lokacemi, proces aktivity převést materiál na výrobky a převodu činnosti přesunout materiál nebo výrobky z jednoho umístění do jiného. Můžete umístění modelu a pracovní buňky jako spravované dodavatele přiřazením účtu dodavatele, skladu nebo prostředku skupiny prostředků.  

Na základě těchto schopností, lean manufacturing nevyžaduje, žádné zvláštní funkce pro podporu toku materiálu a výrobků. Všechny možné scénáře zahrnující dodavatele lze modelovat poskytovatelům služeb na výrobu nebo přepravu na základě architektury výrobní tok a činností.  

Subdodavatele lze použít mimo zásobník materiálu, který je umístěn na subdodavatele. Při manipulačních jednotek jsou vyprázdněny na subdodavatele, kanbanové karty jsou vráceny do buňky sestavení společně s další dodávkou. Zásobník materiálu na subdodavatele, jsou pak doplněny. Převody z subdodavatele a je možné modelovat jako explicitní převod činností na podporu procesu dodávky a vyskladnění. Pokud explicitní registrace není vyžadována k podpoře fyzické přepravy, činnost přenosu lze vynechat.  

Vyrovnání celkové kapacity výrobního toku zatížení lze použít subdodavatele. Například výrobní tok je modelována pomocí naplánované kanban pravidla. Plánovači používá Rada plánovat a načíst úroveň plánování kanbanu obě pracovní buňky na požádání. Plánování také sleduje plán konsolidované dodávky zásobníku materiálu na **plán dodávek** stránky. Více subdodavatelům lze modelovat v jedné nebo více výrobních toků a může být více kanbanových pravidel, které lze použít k zadání stejného produktu do stejného umístění prostřednictvím různých aktivit. Plánování alternativní kanbanové pravidlo kanbanu, který byl původně vytvořen pro interní výrobu alternativní proces přeplánovat převést kanbany. Ve skutečnosti subdodávek povahu pracovní buňka nemá žádný vliv na výrobní tok. Stejné pracovní princip platí pro dva paralelní vnitřní pracovní buňky nebo dvě buňky subdodávek.   

Stejně jako jakékoli jiné činnosti ve výrobním toku subdodavatelské aktivity spotřebovat a zadání zanesených v inventurách, než se nedostalo do inventur (rozpracované \[NV\]) a materiálu polotovarů a výrobků. Postupy pro plánování a provádění subdodavatelských činností ve všech případech jsou stejné. Navíc tyto zpracovat stejné jako postupy pro vnitřní práce.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Nákupní proces pro subdodavatelské aktivity (služby)
Nákupní proces pro subdodavatelské aktivity je založena na fyzický tok materiálu, je registrovanou pokroku kanbanové úlohy, například, spustit nebo dokončit. Finanční tok, například náklady na práce subdodavatele je sekundární tok, který následuje fyzický tok. Ve stejnou dobu nákupní proces je nezávislý proces, který umožňuje ruční úpravy nákupních dokladů u každého kroku. Zde je nákupní proces pro subdodavatelské aktivity:

1.  Vytvořte nákupní smlouvy. Nákupní smlouva je vytvořena pro službu a připojen k aktivity výrobního toku.
2.  Vytvoření nákupní objednávky. Dílčí nákupní objednávky lze vytvořit pro služby, založené na plánované kanbanové úlohy. Úlohy pro stejné služby mohou být seskupeny do řádků nákupní objednávky podle dne, týdne nebo měsíce. Řádky nákupní objednávky lze vytvořit kdykoli po vytvoření kanbanových úloh. Řádky nákupní objednávky lze vytvořit i ve skutečnosti. Tato možnost je obvykle zaškrtnuto, pokud subdodavatele poskytuje služby bez dalších upozornění, podle kanbany nebo kanbanové karty, které obdrží subdodavatele. V tomto případě lze minimalizovat odchylky mezi nákupní objednávky a faktury.
3.  Generovat kanbanové karty, materiál a výdejky k odeslání subdodavateli Příprava na zpracování. Založen na detailní modelování výrobní tok, Příprava se provádí na kanbanové desce pro aktivity procesu pomocí výdejky a příprava funkce. Příprava se provádí také Kanbanová deska pro úlohy převodu pomocí výdejky a zahájení nebo dokončení. Materiál na skladě oba procesy mohou být podporována WMS vyskladnění a dodávky procesu. Na požádání lze vytvořit přepravní doklad.
4.  Generovat kanban manipulačních jednotek a kanbanové karty. Po zpracování, jsou vráceny karty od subdodavatele. Karty obsahují obvykle dodací list, který určuje fyzický materiál, který byl dodán. Odkaz na služby poskytované není vyžadováno. Dodání materiálu nebo produktu u zákazníka, je registrována na kanbanové desce, v závislosti na kanbanové karty. (Pro aktivity procesu kanbanu nebo Kanbanová deska pro úlohy převodu používá, v závislosti na Modelovaný činnosti.).
5.  Vytvoření oznámení o poradní. Poradní příjmu lze nahradit dodacího listu dokumentu pro přijaté služby. Informační zpravodaje příjmu mohou být generovány založené na dokončení kanbanových úloh pro subdodavatelské aktivity pro vybrané období. Pro příjem každé úlohy jsou vytvořeny informační zpravodaje řádku související nákupní objednávky. Poradní oznámení můžete vytisknout a subdodavateli odeslána jako potvrzení o přijetí.
6.  Generování faktury.

Při fakturaci subdodavatele na dobu ukončení procesu. Odpovídající faktury se provádí proti příjem informačních zpravodajů, které jsou vytvořeny. Vzhledem k tomu, že přijetí zpravodaje představují přesné fyzického příjmu materiálu, třícestné párování je zjednodušeno.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurace aktivity pro subdodávky
Následující části popisují, jak nakonfigurovat pro subdodavatelské aktivity.

### <a name="subcontracted-services"></a>Subdodavatelské služby

Platba zboží, který je používán podle činností subdodavatelů, musí být produkt, který má následující vlastnosti:

-   **Typ přípravku:** služby
-   **Skupina skladových modelů:** není na skladě

Tento požadavek zajišťuje použití první v první out (FIFO) skladový model. **Poznámka:** výpočet ceny produktů vyžaduje definovat standardní náklady na servis. Nákupní smlouva s dodavatelem je vyžadován. Službu nelze jinak podle činností subdodavatelů.

### <a name="subcontracted-process-activities"></a>Proces subdodavatelských činností

Chcete-li konfigurovat aktivitu procesu jako aktivitu subdodávek, postupujte takto.

1.  Nastavte buňku práce subdodavatele. Ke konfiguraci pracovní buňky zadána, je nutné vytvořit prostředek **dodavatele** zadejte a přidružit pracovní buňka (skupina prostředků). Kategorie nákladů za běhu **přímý outsourcing** by měl být přiřazen typ nákladové skupiny pracovní buňku. Nákladové kategorie pro nastavení a množství nejsou povinné.
2.  Po vytvoření aktivity procesu a související s buňkou práce subdodavatele, je nutné nakonfigurovat služby pro aktivitu před aktivací verze výrobního toku. Na dokončení tohoto kroku **aktivity****podrobnosti** stránky. U činností, které jsou přidruženy k buňce subdodavatelské práce **podmínky služby** s náhledem se zobrazí. Na této záložce s náhledem přidáte výchozí služba, která je platná pro všechny položky výstup. Vyžadují-li konkrétní výstupní položky různých služeb nebo jinou službu parametry výpočtu (například poměr různých služeb), můžete přidat další služby k aktivitě.

## <a name="subcontracted-transfer-activities"></a>Na činnost přenosu subdodávek
Aktivita převodu je nakonfigurován jako subdodavatelské aktivity, v závislosti na **dopravce** nastavení převodu činnosti. Existují tyto možnosti:

-   **Přepravce** – aktivita je zadána Pokud spravuje přenos ze skladu dodavatele (jak je definován vlastností skladu). Všechny vybrané nákupní smlouvy pro služby musí mít stejné ID dodavatele jako sklad.
-   **Příjemce** – aktivita je zadána Pokud převod na sklad spravuje dodavatele (jak je definován vlastností skladu). Všechny vybrané nákupní smlouvy pro služby musí mít stejné ID dodavatele jako sklad.
-   **Carrier** – aktivita je zadána dodavateli, který poskytuje službu. Platit, dopravce musí být vytvořen pro řízení skladu a musíte mít účet přiřazený dodavatel.

Pro aktivity procesu, je nutné nakonfigurovat výchozí služby pro subdodavatelské přepravní činnost na **podmínky služby** s náhledem **aktivity****podrobnosti** stránky.

## <a name="service-quantity-calculation"></a>Výpočet množství služby
Celý nákupní proces je založen na odkaz na položku služby. Odkaz na tuto položku se měří v měrných služby. Služby se obvykle měří v počtu služeb (jednotky) nebo v čase. Pro výpočet množství servisu na základě registrovaných dokončení kanbanových úloh, můžete použít následující metody:

-   **Výpočet, který je založen na počet úloh** – se rovná jedné kanbanové úlohy *n* jednotky bez ohledu na množství produktu, který je součástí služby. V lean manufacturing, jedna úloha odpovídá jeden manipulační jednotky. Tento způsob výpočtu se vztahuje na všechny služby, které mají pevnou cenu na manipulační jednotku. Proto tato metoda se obvykle týká aktivit převodu. Však můžete také použít proces činností, které zpracovávají celé manipulační jednotky.
-   **Výpočet, který je založen na množství produktu** – množství servisu je vzhledem k množství produktu, které je naplánováno dodány. Při výpočtu množství produktu dodané množství chyb můžete buď zahrnuty nebo vyloučeny. Tento způsob výpočtu se vztahuje na všechny případy, kdy dohodnuté služby cena za jednotku zpracovaných produktů.
-   **Výpočet, který je založen na čas aktivity** – časy teoretické činnosti se počítají, založené na době zpracování aktivity zpracování celkové množství a poměr propustnosti zpracovaného produktu. Tento způsob výpočtu se vztahuje na služby, které jsou placené hodiny a mají odchylky v každém zpracovaného produktu.

## <a name="cost-accounting-of-subcontracted-services"></a>Účtování nákladů služeb subdodavatele
Při zaúčtování příjemky poradní nebo dodavatele dodacího listu nákupní objednávky, která byla vytvořena pro výrobní tok (jinými slovy, nákupní objednávky, která byla generována na základě kanbanových úloh pro subdodavatelské aktivity), je hodnota příjmu zaúčtovány na účty nedokončené výroby výrobního toku. Odchylek faktur jsou také zaúčtovány do výrobní tok. Nákladová kategorie pro subdodavatelské práce byly zavedeny. Tuto nákladovou kategorii povolit průhledné sledování hodnoty subdodavatelské práce, která je přidělena NV a spotřebovaného za období.  

Zpětné účtování nákladů pro lean manufacturing konci ocenění období vypočte skutečné odchylky výrobků, které jsou vyrobeny z výrobního toku během období ocenění.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelování přenosu jako subdodavatelské aktivity
Uživatelé často považují za nevýrobních dopravy a domníváte se přidá žádnou hodnotu. Srovnání nákladů na subdodávky pro interní výrobní náklady však musí být zvážen aktivit dodatečné dopravní náklady. Přepravní náklady v rámci nákladů na dodání výrobků k zákazníkovi by model výrobního toku, které rozložena na více místech a vyžaduje dopravu. 

Podle činností subdodavatelů v lean manufacturing umožňuje integrovat dopravci a dopravy dodavatele, které se přesouvají mezi umístění výrobní tok materiálu a výrobků. Modelování přenosu činnost, můžete přiřadit dopravce nebo dodavatele. Aktivity nebo úlohy převod je založen na služby a nákupní smlouvy a můžete vytvořit nákupní objednávky a příjem informačních zpravodajů, na základě skutečných přenos úloh. Tato funkce je stejná jako funkce pro proces subdodavatelských činností.  

Proto Dynamics 365 pro operace nyní podporuje výpočet Kusovníku, která zahrnuje dopravu, vytvoření související nákupní objednávky, integrované potvrzení registrace a integraci dopravní náklady na servis do nákladů výrobní tok.




