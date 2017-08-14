---
title: "Zpětné účtování nákladů"
description: "Toto téma představuje koncept zpětného účtování nákladů používané pro Lean manufacturing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: 9ea9eb66abf7898ce735e1204259fcc9b9523c52
ms.openlocfilehash: 404803c6317b2aeda78de86d4ba11987b2a8cf65
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="backflush-costing"></a>Zpětné účtování nákladů

[!include[banner](../includes/banner.md)]


Toto téma představuje koncept zpětného účtování nákladů používané pro Lean manufacturing. 

Výpočet nákladů pro Lean manufacturing umožňuje výrobnímu toku použití metody akumulace nákladů, která je označována jako zpětného účtování nákladů. V metodě zpětného účtování nákladů jsou akumulovány přímé materiály, které jsou spotřebovány v účtu nákladů výrobního toku nedokončené výroby (NV). Používá se skupina modelu zásob pro standardní náklady. Produkty, které jsou přijaty z výrobního toku, jsou odečteny od nedokončené výroby na standardní náklady. Hlavní rozdíl mezi zpětným účtováním nákladů a standardními náklady spočívá v tom, že pro zpětné účtování nákladů nebudou odchylky vypočteny na kanban nebo dokončený produkt. Místo toho se odchylky vypočítávají pro výrobní tok za období. Tato metoda představuje skutečně štíhlý koncept pro vykazování spotřeby materiálu. Vyhrazená vyskladněná množství materiálu nejsou vykazována do kanbanu nebo výrobní zakázky. Místo toho jsou pro daný výrobní tok připraveny úplné dávky nebo manipulační jednotky. Po zaregistrování dávek nebo manipulačních jednotek jako prázdných jsou deklarovány jako spotřebované. Může být použita rozšířená spotřeba, v závislosti na [konfiguraci výrobního toku](/dynamics365/unified-operations/supply-chain/production-control/lean-manufacturing-modeling-lean-organization). Než budou organizace moci použít rozšířenou spotřebu, musí umožnit rozplynutí materiálu v NV výrobního toku. Periodické zpětné účtování nákladů určuje efektivní hodnotu nedokončené výroby na konci období. Toto určení vychází z manipulačních jednotek kanbanu a stavu kanbanové úlohy. Odchylky mezi hodnotami platnosti a skutečnými hodnotami NV na nákladovou skupinu a položku jsou zaúčtovány a zobrazí se jako odchylky.

## <a name="configuring-backflush-costing"></a>Konfigurace zpětného účtování nákladů
Pokud chcete povolit výpočet nákladů, musíte dokončit následující nastavení:

-   **Nastavte účty nedokončené výroby pro výrobní tok a skupinu výroby.** Účty nedokončené výroby pro výrobní tok jsou uvedené ve skupině výroby. Tok výroby pro zpětné účtování nákladů vypočítá odchylky jako rozdíl v hodnotě nedokončené výroby před a po spuštění zpětného účtování nákladů pro každý výrobní tok. Proto vám doporučujeme vytvořit účet NV pro každý výrobní tok.
-   **Přiřaďte skupině prostředků kategorii nákladů.** Kategorii nákladů je nutné přiřadit kategorii spuštění pracovní buňky. Pokud chcete určit odchylky podle aktivity, je třeba vytvořit nákladovou kategorii pro každou pracovní buňku. Kategorie nákladů pro nastavení a množství nejsou při výpočtu nákladů pro lean manufacturing zohledněny. Účty nedokončené výroby na skupinu prostředků jsou ve zpětném účtování nákladů ignorovány. Pro subdodavatelské aktivity není potřeba žádná kategorie nákladů. Místo toho se použije nákladová skupina přiřazená k aktivní službě.
-   **Přiřaďte nákladové skupiny.** Pokud chcete povolit segmentaci příspěvku nákladů ve výrobním toku, musíte přiřadit skupiny nákladů podle typu skupiny nákladů:
    -   **Skupina přímých nákladů na materiál** – Přímý materiál vyžaduje nákladovou skupinu, která identifikuje materiálovou kategorii nákladů. Tato nákladová skupina umožňuje agregované zobrazení nákladů, NV a odchylek podle přímého materiálu.
    -   **Nákladová skupina pro přímou výrobu** – Tato skupina zaznamenává příspěvek přímých nákladů na operační zdroje pro výrobní tok. Tato nákladová skupina umožňuje agregované zobrazení nákladů NV a odchylky podle přímých výrobních nákladů.
    -   **Nepřímá nákladová skupina** – tato skupina je požadována za účelem výpočtu příspěvku nepřímých nákladů k výrobnímu toku. Tato nákladová skupina umožňuje agregované zobrazení nákladů NV a odchylky podle nepřímých nákladů.
    -   **Nákladová skupina pro přímý outsourcing** – nákladová skupina pro služby umožňuje agregované zobrazení přiřazených nákladů a NV a určuje odchylky nákladů služeb subdodavatele.
    -   **Nákladová skupina pro dokončený produkt** – Dokončené produkty vyžadují nákladovou skupinu, která identifikuje kategorii produktů pro výpočet nákladů. Tato nákladová skupina umožňuje agregované zobrazení nákladů, NV a odchylek podle kategorie produktu. Standardní náklady pro produkty, které se vypočítávají pomocí výpočtu nákladů založeného na kusovníku (BOM) a výrobním toku a kanbanových pravidlech nebo trasy.

### <a name="costing-sheet"></a>Nákladový formulář

Nákladový formulář modeluje strukturu nákladů pro společnost a je tvořen nákladovými skupinami ke klasifikaci nákladů. V nákladovém formuláři jsou různé formuláře. Zobrazuje informace o nákladech podle struktury, která je v něm určena. V nákladovém formuláři můžete také definovat vzorec, který se použije pro výpočet nepřímých nákladů. Výpočetní vzorec může být založen na množství, hmotnosti, objemu nebo hodnotě.

-   **Definujte verzi pro výpočet nákladů.** V této verzi společnost definuje, jakým způsobem by měly být udržovány náklady. Nákladová verze může obsahovat sadu záznamů o standardních nákladech nebo sadu záznamů o plánovaných nákladech v závislosti na nákladovém typu, který je přiřazený nákladové verzi. Nákladová verze, která se používá pro výpočet nákladů pro Lean manufacturing, musí být založena na standardních nákladech.
-   **Přiřaďte k uvolněným produktům skupinu skladových modelů.** Všechny produkty související s výrobním tokem musí být přiřazeny skupině skladového modelu, která používá skupinu modelu zásob **Standardní náklady**. Standardní náklady jsou uchovávány podle pracoviště a data aktivace. Pro základní produkty lze vybrat skupinu skladových modelů, pokud jsou náklady uchovávány podle varianty nebo hlavního produktu.
-   **Z definice jsou služby subdodavatele služby bez zásob.** Subdodavatelské aktivity nemají žádnou skupinu skladových modelů. Abyste správně stanovili náklady na subdodavatelské aktivity, ujistěte se, že aktivita služby patří do skupiny skladových modelů, kde je zásada zásob nastavena na **Produkt na skladě = False**.

U výsledných produktů vyžaduje výpočet nákladů založený na výrobním toku udržování standardních nákladů pro služby, které se vztahují k subdodavatelským aktivitám. Nákladová skupina, která je přiřazena ke službám, slouží k určení odchylek nákladů subdodavatelské aktivity.

## <a name="cost-calculation-for-lean-manufacturing"></a>Výpočet nákladů pro Lean manufacturing
Pro produkty, které jsou dodávány mimo výrobní tok, musí kalkulace kusovníku vycházet z verze postupu nebo výrobního toku. Výpočet kusovníku vypočítá náklady na produkt a rozpis související s prostředky a materiály, které jsou zapotřebí k vytvoření výrobku. Srážky z účtu NV pro daný výrobní tok se provádí pomocí rozpisu výrobku podle položky a nákladové skupiny.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Výpočet založený na výrobním toku

Lean manufacturing pro Microsoft Dynamics 365 for Finance and Operations nezávisí na postupech. Výpočet nákladů pro produkty, které jsou dodávány z výrobního toku, může vycházet z výrobního toku jako takového. Než bude možné výpočet provést, musí být vytvořeno kanbanové pravidlo, které dodává produkt z výrobního toku. Pokud lze produkt dodat z více z více výrobních toků na stejném pracovišti k datu výpočtu, můžete vybrat výrobní tok pro kalkulaci kusovníku. Na stránce **Výchozí výrobní tok** můžete nakonfigurovat výchozí výrobní tok pro každou položku. Existuje-li více kanbanových pravidel pro stejný produkt ve stejném výrobním toku, který je aktivní k datu výpočtu, výpočet vybere první kanbanové pravidlo, které je aktivní pro výpočet.

### <a name="calculation-that-is-based-on-the-route"></a>Výpočet založený na postupu

Výpočet, který vychází z postupu má stejnou platnost jako výpočet založený na výrobním toku. Výpočet, který je založen na postupu, však nepoužívá také výpočet nákladů pro funkci Lean manufacturing. Postup by měl používat požadavky na prostředek pro skupiny prostředků. Abyste se vyhnuli systematickým odchylkám, měl by také použít stejné pracovní buňky a alespoň stejné nákladové kategorie. Opět platí že byste se měli vyhnout nákladovým kategoriím pro nastavení a množství. Nepomáhají při výpočtu nákladů v podrobnějším rozdělení než zpětný odpočet nákladů v Lean manufacturing. Chcete-li zjistit, která možnost (výrobní tok nebo postup) je vhodnější při výpočtu nákladů, zvažte výsledky rozúčtování nákladů. Verze, která se více blíží realitě a vytváří celkově méně odchylek, je lepší možnost. V prostředí Lean manufacturing, kde je produkt poskytnutý z jednoho výrobního toku a jednoho kanbanového pravidla, je pravděpodobně přesnější výpočet založený na výrobním toku. U produktu, který může dodat Lean manufacturing a výrobní zakázky na stejném pracovišti nebo který má více výrobních toků nebo více kanbanových pravidel, může být výpočet přesnější, pokud je založen na verzi postupu, která je vytvořena pro výpočet ceny, nikoli pro výrobu. Výpočet výrobního toku musí být použit pro výpočet produktů, které se týkají subdodávky. V aplikaci Microsoft Dynamics 365 for Finance and Operations pro subdodávky prostřednictvím výrobních zakázek a subdodávky v Lean manufacturing se používají dva různé přístupy. Lean manufacturing zavádí nový typ skupiny nákladů, **Přímý outsourcing**, k výpočtu subdodavatelských služeb.

## <a name="material-consumption"></a>Spotřeba materiálu
Když se materiál spotřebovává ze skladu pro nedokončenou výrobu, náklady na materiál jsou přidány do nedokončené výroby při skutečných standardních nákladech pro nákladovou skupinu. Tato operace se provádí při splnění následujících podmínek:

-   Kanbanové výdeje jsou zaúčtovány pro řádky výdeje, které aktualizují zásoby.
-   Jsou dokončeny úlohy převodu, které aktualizují stav zásob při výdeji, ale ne při příjmu (převod materiálu ze zásob do nedokončené výroby).

## <a name="receiving-products-from-the-production-flow"></a>Přijetí produktů z výrobního toku
Produkty jsou z výrobního toku přijímány při splnění následujících podmínek:

-   Jsou dokončeny úlohy procesu, které mají možnost **Aktualizovat zásoby při příjmu** nastavenou na **Ano**.
-   Úlohy převodu jsou dokončeny, které aktualizují zásoby na příjemce, ale mají možnost **Aktualizovat zásoby na sadě vyskladnění** nastavenou na **Ne** (převod z nedokončené výroby). Tato možnost umožňuje přijmout jakékoli produkty z výrobního toku bez ohledu na konfiguraci kusovníku a postupu. Proces sleduje pouze fyzické toky. Tato možnost je obzvlášť vhodná pro příjem vedlejších produktů, produktů nebo vyřazených produktů z výrobního toku a pro opravy zůstatku nákladů nedokončené výroby výrobního toku odpovídajícím způsobem.

Produkty, které jsou přijaty z výrobního toku, jsou odečteny z nedokončené výroby.

## <a name="products-in-wip"></a>Produkty v nedokončené výrobě
Model NV pro Lean manufacturing v Microsoft Dynamics 365 for Finance and Operations umožňuje využití stavu manipulační jednotky kanbanu ke správě materiálu, polotovarů a dokončených produktů, které jsou součástí nedokončené výroby.

-   **Přiřazeno** – kanban může mít spotřebovaný materiály, který je zaúčtován v nedokončené výrobě.
-   **Přijaté** - Pokud kanban odkazuje na poslední aktivitu, kde je možnost **Aktualizovat zásoby při příjmu nastavena na** **Ne**, představuje plnou manipulační jednotku produktu nebo polotovaru, který není zaregistrován v zásobách.

Všimněte si, že materiál v nedokončené výrobě není viditelný v přehledu zásob na skladě. Je však vidět v přehledech kanbanového množství.

## <a name="consuming-products-in-wip"></a>Spotřeba produktů v nedokončené výrobě
Produkty v nedokončené výrobě jsou spotřebovány, když jsou odpovídající manipulační jednotky kanbanu prázdné. Prázdný signál kanbanu nevytváří aktivní nákladové transakce, ale projeví se až po spuštění následující zpětného účtování nákladů. Vyprázdněné manipulační jednotky kanbanu již nejsou účtovány jako množství na skladě a tedy vypočteny jako spotřebované v období.

### <a name="automatic-empty-registration"></a>Automatická prázdná registrace

Naplánované kanbany nebo kanbany události může být nastavit na automatickou prázdnou registraci v kanbanovém pravidle:

-   **Při příjmu manipulačních jednotek** – ve výchozím nastavení pro plánované kanbany je materiál deklarován jako spotřebovaný po dokončení poslední úlohy kanbanu. Pro kanbany pro pevné množství se tato možnost doporučuje pouze pro jednopřihrádkové kanbany, protože vrací karty se zdrojem poptávky při každém zaznamenání příjmu kanbanu v konečném místě určení.
-   **Pokud je požadavek na zdroj registrován** – tato možnost je dostupná pouze pro kanbany události a je pro ně výchozí možností. V souvislosti s nedokončenou výrobou je tato možnost užitečná v případě snahy o zachování čisté nedokončené výroby, protože kanbany pro komponenty v nedokončené výrobě jsou vyprázdněny automaticky a tím pádem spotřebovávány z nedokončené výroby, když je připraven nadřazený kanban.

Závěrem – lze přiřadit manipulační jednotky kanbanu (v procesu =), přijaté (= podrobné) nebo prázdné. Neexistuje žádné částečné vyprazdňování. Proto platí, že pokud chcete povolit přesnou registraci spotřeby, je důležité omezit množství produktu v kanbanu, aby byly nižší než spotřeba za dané období. Produkty, které se přesouvají do dílenského řízení ve velkých dávkách, které zahrnují dny nebo týdny poptávky, by neměly být spotřebovány pro nedokončenou výrobu. Místo toho je nutné tyto produkty uchovávat ve skladu.

## <a name="backflush-costing"></a>Zpětné účtování nákladů
Je třeba spustit zpětné účtování nákladů pro pravidelné ocenění nedokončené výroby a výrobu stavu konce období pro výpočet odchylky materiálu, práce a nepřímých nákladů pro výrobu. Vypočtené odchylky jsou zaúčtovány na účty odchylek. V procesu zpětného účtování nákladů se používají všechny výrobní toky právnické osoby v rámci stejné dávky spuštění. Když je zpětné účtování nákladů v dávce, zpracování může mít více podprocesů ve výrobním toku. Období zpětného účtování je definováno koncovým datem. Nelze zaúčtovat nové transakce k datu, kdy již byl proveden výpočet zpětného účtování nákladů. Nikdy byste neměli spouštět zpětné účtování nákladů pro aktuální datum předtím, než tento den skutečně uplyne. Výpočet zpětného účtování nákladů provede následující kroky.

1.  Určete nevyužité množství ve výrobním toku jako koncové datum období. Po spuštění zpětného účtování nákladů můžete zobrazit nevyužitá množství k datu spuštění nákladů v dialogovém okně **Nevyužité množství**.
2.  Vypočítejte čistou realizovanou spotřebu výroby za období.
3.  Vymažte nedokončenou výrobu z realizované spotřeby prostředků a produktů.
4.  Výpočet výrobních odchylek standardních nákladů pro období. **Pro komponenty spotřebované za období:**
    -   Finančně aktualizujte realizované čisté množství materiálu, který výrobní tok spotřeboval za období. Systém zpracovává v pořadí první do skladu, první ze skladu (FIFO) pro jednotlivé skladové transakce tak, aby finančně aktualizoval fyzicky aktualizované transakce pro daný výrobní tok, dokud není dosaženo realizované čisté množství za období.
    -   Transakce jsou finančně rozděleny tak, aby mapovaly přesné spotřebované množství.
    -   Nevyužité množství v nedokončené výrobě výrobního toku zůstane ve fyzicky aktualizovaném stavu.

    **Dokončená množství výroby za období:**
    -   Finančně aktualizujte skladové transakce pro dokončená množství za období.

    **Náklady na převod:**
    -   Použité transakce převodu nákladů (transakce postupu), které byly zaznamenány za období, jsou finančně aktualizovány.
    -   Všechny přímé výrobní náklady jsou finančně aktualizovány. Všechny úlohy kanbanových procesů, které jsou dokončeny během období, jsou akumulovány.
    -   Všechny nepřímé náklady vypočítané pro spotřebovaný materiál v rámci období jsou vypočteny a odečteny od nepřímé výroby. Zbývající nepřímé náklady jsou zaúčtovány jako odchylka.

5.  Vypočítejte výrobní odchylky standardních nákladů pro období. Odchylku lze vypočítat za nákladovou skupinu.






