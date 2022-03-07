---
title: Subdodávky na základě aktivit
description: Toto téma podrobně popisuje, jak používat subdodavatelské aktivity ve výrobním toku pro lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule, PlanActivityServiceDetails, PlanActivityServiceWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4217b78d53529572f1ae5e99fbd1ed5c233569f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246518"
---
# <a name="activity-based-subcontracting"></a>Subdodávky na základě aktivit

[!include [banner](../includes/banner.md)]

Toto téma podrobně popisuje, jak používat subdodavatelské aktivity ve výrobním toku pro lean manufacturing.

V aplikaci Microsoft Dynamics 365 Supply Chain Management existují dva přístupy k subdodávkám: výrobní zakázky a lean manufacturing. V přístupu lean manufacturing je subdodavatelská práce modelována jako služba, která souvisí s aktivitou výrobního toku. Zavádíme speciální typ nákladové skupiny s názvem **Přímý outsourcing** a subdodavatelské služby již nebudou součástí kusovníku. Nákladové účetnictví subdodavatelské práce je plně integrováno do řešení výpočtu nákladů pro lean manufacturing.

## <a name="production-flows-that-involve-subcontractors"></a>Výrobní toky, které zahrnují subdodavatele
Základní princip výrobního toku se při subdodavatelských aktivitách nijak nemění. Materiál se stále pohybuje mezi lokacemi, aktivity proces převádí materiál na výrobky a aktivity převodu přesouvají materiál nebo výrobky z jednoho místa do druhého. Můžete modelovat lokace a pracovní buňky jako spravované dodavateli přiřazením účtu dodavatele ke skladu nebo prostředku skupiny prostředků.  

Na základě těchto schopností nevyžaduje lean manufacturing žádné zvláštní funkce pro podporu toku materiálu a výrobků. Všechny možné scénáře zahrnující dodavatele jako poskytovatele výroby nebo přepravních služeb lze modelovat na základě architektury výrobního toku a činností.  

Například subdodavatel vychází ze zásobníku materiálu, který je umístěn na straně subdodavatele. Když jsou manipulační jednotky vyprázdněny na straně subdodavatele, kanbanové karty jsou vráceny do buňky sestavení společně s další dodávkou. Zásobník materiálu na straně subdodavatele je poté doplněn. Převody k subdodavateli a od něj je možné modelovat jako explicitní aktivity převodu na podporu procesu dodávky a vyskladnění. Pokud není explicitní registrace vyžadována k podpoře fyzické přepravy, aktivity převodu lze vynechat.  

K vyrovnání zatížení celkové kapacity výrobního toku lze použít subdodavatele. Například výrobní tok je modelován pomocí plánových pravidel kanbanu. Plánovač používá desku kanbanového plánování pro naplánování a vyrovnání zátěže obou pracovních buněk poptávky. Plánovač také sleduje plán konsolidované dodávky pro zásobník materiálu na stránce **Plán dodávek**. Více subdodavatelů lze modelovat v jednom nebo více výrobních tocích a může existovat více kanbanových pravidel, která lze použít k dodání stejného produktu do stejného umístění prostřednictvím různých aktivit. Plánovač může převést kanbany na alternativní kanbanové pravidlo, aby došlo k přeplánování kanbanu, který byl původně vytvořen pro interní výrobu, na alternativní proces. Ve skutečnosti nemá subdodavatelská povaha pracovní buňky žádný vliv na výrobní tok. Stejné pracovní principy platí pro dvě paralelní interní pracovní buňky nebo pro dvě subdodavatelské buňky.   

Stejně jako jakékoli jiné aktivity ve výrobním toku mohou subdodavatelské aktivity spotřebovávat a dodávat materiály a výrobky, které jsou uvedeny v zásobách, nejsou uvedeny v zásobách (nedokončená výroba \[NV\]) nebo mají podobu polotovarů. Postupy pro plánování a provádění subdodavatelských aktivit jsou ve všech případech stejné. Navíc jsou tyto procesy stejné jako procesy pro interní práci.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Nákupní proces pro subdodavatelské aktivity (služby)
Nákupní proces pro subdodavatelské aktivity je založen na fyzickém toku materiálu, který je registrovaný postupem kanbanové úlohy, například Spustit nebo Dokončit. Například finanční tok, náklady na dodavatelskou práci, je sekundární tok, který následuje fyzický tok. Ve stejnou dobu je nákupní proces nezávislým procesem, který umožňuje ruční úpravy nákupních dokladů u každého kroku. Zde je nákupní proces pro subdodavatelské aktivity (služby):

1.  Vytvořte nákupní smlouvy. Nákupní smlouva je vytvořena pro službu a připojena k aktivitě výrobního toku.
2.  Vytvoření nákupní objednávky. Dílčí nákupní objednávky lze vytvořit pro služby, na základě plánovaných kanbanových úloh. Úlohy pro stejnou službu mohou být seskupeny do řádků nákupní objednávky podle dne, týdne nebo měsíce. Řádky nákupní objednávky lze vytvořit kdykoli po vytvoření kanbanových úloh. Řádky nákupní objednávky lze dokonce vytvořit i poté. Tato možnost je obvykle zvolena tehdy, když subdodavatel poskytuje služby bez dalších upozornění, podle kanbanů nebo kanbanových karet, které subdodavatele obdrží. V tomto případě lze minimalizovat odchylky mezi nákupní objednávkou a fakturou.
3.  Vygenerujte kanbanové karty, materiál a výdejky pro odeslání subdodavateli na přípravu ke zpracování. Na základě detailního modelování výrobního toku se příprava provádí na kanbanové desce pro aktivity procesu pomocí výdejky a funkce přípravy. Případně se příprava provádí také na kanbanová desce pro úlohy převodu pomocí výdejky a zahájení nebo dokončení. Pro materiál na skladě lze oba procesy podporovat pomocí procesu WMS-výdejky a dodávky. Na požádání lze vytvořit přepravní doklad.
4.  Vygenerujte manipulační jednotky kanbanu a kanbanové karty. Po zpracování jsou vráceny karty od subdodavatele. Karty obsahují obvykle poznámku k dodání, která určuje fyzický dodaný materiál. Odkaz na poskytované služby není vyžadován. Doručení materiálu nebo produktu u zákazníka je registrováno na kanbanové desce, v závislosti na kanbanových kartých. (V závislosti na modelovaných aktivitách se použije buď kanbanová deska pro aktivity procesu nebo kanbanová deska pro úlohy převodu.).
5.  Vytvořte avízo o přijetí. Avízo o přijetí lze pro přijaté služby použít jako náhradu ze dokument dodacího listu. Avíza o přijetí lze vygenerovat na základě dokončených kanbanových úloh pro subdodavatelské aktivity za vybrané období. Pro příjem každé úlohy jsou vytvořena avíza pro související řádky nákupní objednávky. Avízo o přijetí můžete vytisknout a odeslat subdodavateli jako potvrzení o přijetí.
6.  Vygenerujte fakturu.

Proces skončí, když je dodavatel za období vyfakturován. Párování faktury se provádí proti vytvořeným avízům o přijetí. Vzhledem k tomu, že avíza o přijetí představují přesné fyzické přijetí materiálu, je zjednodušené třícestné párování.

## <a name="configuring-activities-for-subcontracting"></a>Konfigurace aktivit pro subdodávky
Následující části popisují, jak nakonfigurovat aktivity pro subdodávky.

### <a name="subcontracted-services"></a>Subdodavatelské služby

Platební položka, která se používá u subdodávek na základě aktivit, musí být produktem, který má následující vlastnosti:

-   **Typ produktu:** Služba
-   **Skupina modelů zásob:** Neskladová

Tento požadavek zajišťuje použití modelu zásob FIFO. **Poznámka:** Výpočet nákladů na produkt vyžaduje, aby byly definovány standardní náklady na službu. Nákupní smlouva s dodavatelem je vyžadována. Službu nelze jinak použít u subdodávek na základě aktivit.

### <a name="subcontracted-process-activities"></a>Aktivity subdodavatelského procesu

Chcete-li konfigurovat aktivitu procesu jako subdodavatelskou aktivitu, postupujte takto.

1.  Nakonfigurujte subdodavatelskou pracovní buňku. Ke konfiguraci pracovní buňky jako subdodavatelské je nutné vytvořit prostředek typu **Dodavatel** a přidružit ho k pracovní buňce (skupině prostředků). Nákladová kategorie typu nákladové skupiny **Přímý outsourcing** musí být přiřazena k pracovní buňce. Nákladové kategorie pro nastavení a množství nejsou povinné.
2.  Po vytvoření aktivity procesu a navázání na subdodavatelskou pracovní buňku je nutné nakonfigurovat službu pro aktivitu před tím, než můžete aktivovat verzi výrobního toku. Tento krok dokončíte na stránce **Podrobnosti o** **aktivitě**. U činností, které jsou přidruženy k subdodavatelské pracovní buňce, se zobrazí pevná záložka **Podmínky služby**. Na této pevné záložce přidejte výchozí službu, která je platná pro všechny výstupní položky. Vyžadují-li konkrétní výstupní položky různé služby nebo různé parametry výpočtu služby (například poměr různých služeb), můžete přidat další služby k aktivitě.

## <a name="subcontracted-transfer-activities"></a>Aktivity subdodavatelského převodu
Aktivita převodu je nakonfigurován jako subdodavatelská aktivita, v závislosti na nastavení aktivity převodu **Dopravce**. Existují tyto možnosti:

-   **Přepravce** – Aktivita je subdodavatelská, pokud je převod ze skladu řízen dodavatelem (jak je definováno vlastností skladu). Všechny vybrané nákupní smlouvy pro služby musí mít stejné ID dodavatele jako sklad.
-   **Příjemce** – Aktivita je subdodavatelská, pokud je převod do skladu řízen dodavatelem (jak je definováno vlastností skladu). Všechny vybrané nákupní smlouvy pro služby musí mít stejné ID dodavatele jako sklad.
-   **Dopravce** – Aktivita je zadána dodavateli, který poskytuje službu. Aby byl dopravce platný, musí být vytvořen pro řízení skladu a musí mít přiřazený dodavatelský účet.

Pokud jde o aktivity procesu, je nutné nakonfigurovat výchozí službu pro aktivity subdodavatelského převodu na pevné záložce **Podmínky služby** stránky **Podrobnosti o** **aktivitě**.

## <a name="service-quantity-calculation"></a>Výpočet množství služby
Celý nákupní proces je založen na odkazu položky pro službu. Tento odkaz položky se měří v měrné jednotce služby. Služby se obvykle měří buď v počtu služeb (jednotky) nebo v čase. Pro výpočet množství služeb na základě registrovaných dokončení kanbanových úloh můžete použít následující metody:

-   **Výpočet, který je založen na počtu úloh** – Jedna kanbanová úloha se rovná počtu *n* jednotek služby, bez ohledu na množství dodaného produktu. V lean manufacturingu odpovídá jedna úloha jedné manipulační jednotce. Tato metoda výpočtu se vztahuje na všechny služby, které mají pevnou cenu za manipulační jednotku. Proto se tato metoda obvykle používá na aktivity převodu. Lze však rovněž použít na aktivity procesu, které zpracovávají manipulační jednotky.
-   **Výpočet, který je založen na množství produktu** – Množství služeb je relativní vzhledem k množství produktu, které je naplánováno/dodáno. Při výpočtu dodaného množství produktu lze buď zahrnout nebo vyloučit množství chyb. Tato metoda výpočtu se vztahuje na všechny případy, kdy je cena služby za jednotku zpracovaného produktu odsouhlasená.
-   **Výpočet, který je založen na času aktivity** – Časy teoretické aktivity se počítají na základě času zpracování aktivity, celkového zpracovaného množství a poměru propustnosti zpracovaného produktu. Tato metoda výpočtu se vztahuje na služby, které jsou placené hodinově a mají odchylky v čase na zpracovaný produkt.

## <a name="cost-accounting-of-subcontracted-services"></a>Nákladové účetnictví subdodavatelských služeb
Když je zaúčtováno avízo o přijetí nebo dodací list dodavatele na nákupní objednávce, která byla vytvořená pro výrobní tok (jinými slovy, na nákupní objednávce, která byla generována na základě kanbanových úloh pro subdodavatelské aktivity), je hodnota přijetí zaúčtována v účtech NV výrobního toku. Odchylky faktur jsou také zaúčtovány do výrobního toku. Byla zavedena nákladová kategorie pro subdodavatelské práce. Tato nákladová kategorie umožňuje jasnější sledování hodnoty subdodavatelské práce, která je přidělena do NV a spotřebována za období.  

Zpětné účtování nákladů pro lean manufacturing na konci nákladového období vypočte skutečné odchylky výrobků, které jsou vyrobeny z výrobního toku během nákladového období.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelování převodů jako subdodavatelských aktivit
Lidé často považují dopravu za nevýrobní a domnívají se, že nepřináší žádnou přidanou hodnotu. Nicméně při srovnání nákladů na subdodávky s náklady interní výroby je třeba vzít náklady na dodatečné přepravní aktivity do úvahy. Výrobní tok, který zahrnuje více lokací a vyžaduje přepravní služby, musí modelovat náklady na dopravu jako součást nákladů na dodání výrobků odběrateli. 

Subdodávky na základě aktivit v lean manufacturingu vám umožňují integrovat dopravce a dodavatele přepravy, kteří přesouvají materiál a výrobky mezi místy výrobního toku. Modelováním aktivity převodu můžete přiřadit dopravce nebo dodavatele. Aktivity/úlohy převodu jsou založeny na službě a nákupní smlouvě a lze vytvořit nákupní objednávky a avíza o přijetí na základě skutečných úloh převodu. Tato funkce je stejná jako funkce pro proces subdodavatelských aktivit.  

Supply Chain Management nyní podporuje výpočet kusovníku, který zahrnuje přepravní služby, vytvoření souvisejících nákupních objednávek, integrovanou registraci příjmu a integraci nákladů na přepravní služby do výpočtu nákladů výrobního toku.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]