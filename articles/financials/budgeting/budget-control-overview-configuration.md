---
title: "Přehled kontrol rozpočtu"
description: "Tento článek obsahuje základní informace o kontrole rozpočtu a poskytuje informace, které umožňují konfiguraci kontroly rozpočtu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, abyste mohli spravovat finančních prostředky."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 60493
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98b5620b343a87426aab13997d1f2e5f7dc30d50
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="budget-control-overview"></a>Přehled řízení 

[!include[banner](../includes/banner.md)]


Tento článek obsahuje základní informace o kontrole rozpočtu a poskytuje informace, které umožňují konfiguraci kontroly rozpočtu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, abyste mohli spravovat finančních prostředky.

<a name="overview"></a>Přehled
--------

Kontrola rozpočtu v aplikaci Microsoft Dynamics 365 for Finance and Operations podporuje správu finančních prostředků v organizaci prostřednictvím účtové osnovy, workflowů, skupin uživatelů, zdrojových dokumentů a deníků, konfigurovatelného výpočtu dostupných finančních prostředků, rozpočtových cyklů a prahových hodnot. Když jsou prvky řízení zavedené, organizace může plánovat, měřit, spravovat a předvídat své finanční prostředky během celého fiskálního roku. 

Po schválení rozpočtů v aplikaci Finance and Operations můžete použít plány rozpočtu ke generování položek registru rozpočtu pro zaznamenání rozpočtu výdajů pro organizaci. Případně můžete vytvořit nebo importovat položky registru rozpočtu z programu třetí strany namísto použití funkce plánování rozpočtu. 

Výdaje lze zaznamenat pomocí hlavních účtů a finančních dimenzí. Můžete nakonfigurovat kontrolu celkových výdajů podle zásad a požadavků organizace, a to seskupením kombinací finančních dimenzí a hlavních účtů. 

Následující graf znázorňuje místo kontroly rozpočtu ve fázích typického rozpočtového cyklu.

[![Rozpočtový cyklus](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Můžete konfigurovat kontrolu rozpočtu podle několika faktorů:

-   **Finanční dimenze**: Jaké finanční dimenze je nutné použít pro vykazování rozpočtu a skutečných hodnot a jaké finanční dimenze jsou potřebné k řízení rozpočtu? Existují určité kombinace dimenzí nebo hlavních účtů, které vyžadují zvláštní pozornost? Existuje například požadavek na sledování rozpočtu a skutečných hodnot podle nákladového střediska a programu? Vyžadují cestovní výdaje zvláštní pozornost?
-   **Čas**: Jaké časové období (fiskální období, fiskální období k datu atd.) se použije k vyhodnocení dostupných rozpočtových prostředků?
-   **Zdrojové dokumenty** – jaké zdrojové dokumenty musí být vyhodnoceny pro kontrolu rozpočtu? By měly být dokumenty hodnoceny podle řádku nebo podle dokumentu?
-   **Výpočet dostupných prostředků**: Mají být dokumenty, jako například nákupní žádanky (předběžná břemena) a nákupní objednávky (břemena) zohledněny ve výpočtu dostupných finančních prostředků? Mají být dokumenty ve stavu konceptu zohledněny ve výpočtu?
-   **Oprávnění pro přepis**: Kdo má oprávnění přesáhnout dostupný rozpočet?

Kontrola rozpočtu je plně integrovaná do aplikace Finance and Operations. Proto je možné vyhodnotit dostupný rozpočet pro plánované nákupy i skutečné nákupy. Jsou k dispozici dotazy a sestavy týkající se rozpočtu. Proto mohou uživatelé vyhodnotit rozpočet v rámci rozpočtového cyklu a podle potřeby provést ve formě revizí či převodů rozpočtu. Správce rozpočtu může také podle potřeby exportovat rozpočet a skutečné hodnoty do aplikace Microsoft Excel kvůli lepší analýze a prognóze.

## <a name="configuring-budget-control"></a>Konfigurace kontroly rozpočtu
### <a name="budget-cycle-time-span"></a>Délka rozpočtového cyklu

Po dokončení konfigurace základního rozpočtování můžete definovat čas nebo počáteční a koncové období pro rozpočtování a kontrolu rozpočtu na stránce **Délka rozpočtového cyklu**. Rozpočtové cykly často odpovídají fiskálním kalendářům mohou však překlenovat fiskální roky.

Další kroky konfigurace se provádí na různých kartách stránky **Konfigurace kontroly rozpočtu**.

### <a name="define-parameters"></a>Definovat parametry

Na základě finančních dimenzí povolených pro rozpočet můžete použít všechny finanční dimenze nebo jejich podmnožinu pro kontrolu rozpočtu. 

Kromě toho lze určit výchozí časový interval (například **Fiskální rok**, **Fiskální rok k datu**, **Fiskální období** nebo **Kvartálně**), podle kterého bude provedena kontrolu rozpočtu v souvisejícím časovém rozpětí rozpočtového cyklu. Můžete také určit manažera rozpočtu výchozí a prahovou hodnotu, která umožní upozornit uživatele na dosažení prahu. Hodnoty v těchto polích budou použity jako výchozí hodnoty ve všech nových pravidlech kontroly rozpočtu nebo rozpočtové skupině, která je vytvořena. Výchozí hodnoty však můžete změnit pro jednotlivé skupiny nebo pravidla. 

Způsoby vytváření a zaznamenání rozpočtů do registru rozpočtu umožňují určit časové rozpětí, které je vybráno při vyhodnocení dostupných rozpočtových prostředků. Je-li vytvořena a použita částka rozpočítaná na roční období pro kombinaci hodnot dimenze, přístup typu Fiskální rok nebo Fiskální rok k datu může být správný. Pokud však organizace, která vytvoří rozpočty podle fiskálního období nebo přidělení k fiskálnímu období, požaduje podrobnější kontrolu, může zvážit použití časových rozpětí Fiskální období k datu nebo Kvartálně. 

Kromě toho může při definování konfigurace pomoci také kultura organizace, protože se týká tvorby rozpočtu a kontroly rozpočtu.

### <a name="over-budget-permissions"></a>Oprávnění překročit rozpočet

Na kartě **Oprávnění překročit rozpočet** můžete určit skupiny uživatelů. Můžete také určit, zda mají uživatelé, kteří jsou členy skupiny, oprávnění překročit rozpočet. Můžete zabránit uživatelům v překročení rozpočtu přes rozpočtový práh, která je nastavený na stránce **Parametry rozpočtu**, nebo jim můžete zabránit v překročení rozpočtu o jakoukoli částku bez ohledu na prahovou hodnotu. Podle toho, jak proaktivně organizace řídí své výdaje, mohou tato oprávnění pomoci spravovat příslušné finanční prostředky. 

### <a name="budget-funds-available"></a>Dostupné rozpočtové prostředky

Na kartě **Dostupné rozpočtové prostředky** můžete definovat vzorec, který se použije k výpočtu dostupných rozpočtových prostředků. V závislosti na tom, jak konzervativně organizace spravuje své finanční prostředky, nebo v závislosti na předpisech a oborových požadavcích může výpočet zahrnovat rozpracované nebo nezaúčtované dokumenty. 

> [!NOTE] 
> Pokud je tento výpočet po upraven během rozpočtového cyklu, tyto změny neovlivní žádné dokumenty, které dříve prošly kontrolami rozpočtu a které byly zaúčtovány či dokončeny.

### <a name="documents-and-journals"></a>Dokumenty a deníky

Na kartě **Dokumenty a deníky** můžete vybrat, které zdrojové dokumenty a deníky budou podrobeny kontrole rozpočtu a zda ke kontrole dojde na úrovni položky řádku nebo celého dokumentu. 

Měli byste spárovat zdrojové dokumenty, které jsou vybrány zaškrtávacími políčky pro zůstatky zahrnuté ve výpočtu dostupných rozpočtových prostředků. Pokud vyberete například položku **Rezervace rozpočtu pro břemena**, měli byste vybrat možnost **Nákupní objednávky**. Při provádění kontroly rozpočtu pro částky a účty v nákupním řádku je k rezervaci přiřazena kategorie kontroly rozpočtu **Břemeno**. Když je kontrola rozpočtu prováděna z hlediska částek a účtů na nákupní žádance, kategorie kontroly rozpočtu přiřazená k rezervaci bude **Předběžné břemeno**. 

Pokud je do výpočtu dostupných rozpočtových prostředků zahrnuta položka **Rezervace rozpočtu pro břemena** a/nebo **Rezervace rozpočtu pro předběžné břemeno** a je třeba je reflektovat zaúčtováním do hlavní knihy, povolte závazkové účtování na stránce **Parametry hlavní knihy**.  

### <a name="assign-budget-models"></a>Přiřadit rozpočtové modely

Na kartě **Přiřadit rozpočtové modely** můžete přiřadit rozpočtové modely k délkám rozpočtových cyklů, které mají být zahrnuty v kontrole rozpočtu.

### <a name="define-budget-control-rules"></a>Definovat pravidla kontroly rozpočtu

Na kartě **Definovat pravidla kontroly rozpočtu** je nutno vytvořit konkrétní pravidla na základě finančních dimenzí, které jsou povolené pro kontrolu rozpočtu. Pokud například platí zaměření na výdaje nebo rozsah výdajů pro oddělení, nastavení na této kartě lze použít k definování a vyhodnocení těchto výdajů. Můžete definovat různé prahové hodnoty pro každé pravidlo kontroly rozpočtu. 

> [!Important]
> Kontrola rozpočtu bude povolena pro každý hlavní účet typu **Zisk a ztráta**, **Výdaj**, **Výnosy, Rozvaha, Pasiva, Jmění** nebo **Majetek**. Pokud je na této kartě pravidlo s prázdným kritériem, bude povolena kontrola rozpočtu **všech** kombinací finančních dimenzí, které zahrnují hlavní účty těchto typů. Proto ověřte, že vytvoříte pravidla kontroly rozpočtu definující pouze rozsahy kombinací finančních dimenzí, u kterých je aktivace kontroly rozpočtu důležitá.  

### <a name="select-main-accounts"></a>Vybrat hlavní účty

Pokud možnost **Hlavní účet** není vybrána jako dimenze kontroly rozpočtu na stránce **Definovat parametry**, ale jsou spravovány konkrétní výdaje, můžete tyto výdaje vybrat na kartě **Vybrat hlavní účty**. Pokud je vybrána možnost **Hlavní účet** jako dimenze kontroly rozpočtu, nejsou vyžadovány žádné položky.  

### <a name="define-budget-groups"></a>Definovat rozpočtové skupiny

Na kartě **Definovat rozpočtové skupiny** lze volitelně definovat jedinečné kombinace finančních dimenzí, kde jsou rozpočtové prostředky shromážděny pro sekundární rozpočtovou kontrolu. Můžete vytvořit jeden záznam, který zahrnuje celou organizaci, nebo lze definovat více skupin představujících jednotlivá oddělení nebo nákladová střediska.  

### <a name="define-message-levels"></a>Definovat úrovně zpráv

Pokud mají být potlačena upozornění na kontrolu rozpočtu pro jakékoli uživatelské skupiny, můžete tyto skupiny určit na stránce **Definovat úrovně zpráv**. Členové skupin uživatelů budou i nadále přijímat chybové zprávy při překročení dostupných rozpočtových prostředků na základě svých oprávnění pro překročení rozpočtu.

### <a name="activate-budget-control"></a>Aktivovat kontrolu rozpočtu

Po konfiguraci kontroly rozpočtu ji můžete zapnout nebo aktivovat na kartě **Aktivovat kontrolu rozpočtu**. Pracovní verze potom vstoupí v platnost.
> [!Important]
> Po zapnutí a aktivaci kontroly rozpočtu a zaúčtování transakcí by vypnutí kontroly nemělo proběhnout v průběhu roku. Když je kontrola rozpočtu vypnuta, aktivity nejsou zaznamenávány pro účely kontroly rozpočtu, takže kontroly rozpočtu se již neprovádí. Dokumenty, které již byly zaúčtovány, tedy nemusí správně odrážet jakékoli uvolněné částky a zůstatky v dotazech a sestavách, které souvisejí s kontrolou rozpočtu. Patří mezi ně statistika kontroly rozpočtu pro jakékoli podřízené nebo upravující dokumenty a deníky. 

Také pamatujte, že transakce, včetně položek registru rozpočtu, které byly zaúčtovány před zapnutím kontroly rozpočtu, nejsou v kontrole rozpočtu zohledněny. Proto je vhodné zapínat kontrolu rozpočtu pouze na začátku nového rozpočtového cyklu. Zajistěte, aby u položek registru rozpočtu, které obsahují počáteční zůstatky rozpočtu pro kontrolu rozpočtu, docházelo k aktualizacím zůstatků rozpočtu pouze po zapnutí kontroly rozpočtu. Jakýkoli otevřený dokument (například nákupní objednávka) bude zkontrolován z hlediska dostupných rozpočtových prostředků a získá rezervaci rozpočtu pro kontrolu rozpočtu, když uživatel ručně spustí kontrolu rozpočtu v dokumentu.

## <a name="using-budget-control"></a>Používání kontroly rozpočtu
Jakmile bude zapnuta kontrola rozpočtu, uživatelům se budou zobrazovat varovné a chybové zprávy týkající se kontroly rozpočtu v dokumentech a denících, které jsou nakonfigurované pro kontrolu rozpočtu. Nezapomeňte, že kontrolu rozpočtu můžete nakonfigurovat tak, aby uživatelé byli upozorněni, pokud překročí rozpočtové prostředky, stále však mohou transakci potvrdit nebo zaúčtovat. Uživatelé mohou prohlížet podrobnosti neúspěšné kontroly rozpočtu na stránce **Chyby a upozornění kontroly rozpočtu**.   

Z této stránky mohou uživatelé přejít na stránku **Statistika kontroly rozpočtu podle období** a zobrazit zde podrobnosti o dostupnosti rozpočtu a rezervace pro vybrané kombinace dimenzí kontroly rozpočtu. Uživatelé mohou také přejít k podrobnostem na stránce **Statistika kontroly rozpočtu** a zobrazit si dostupnost rozpočtu pro všechny kombinace finančních dimenzí, které se používají v kontrole rozpočtu. 

Pokud je kontrola rozpočtu zapnuta pro nákupní objednávky, může správce rozpočtu použít pracovní prostor **Rozpočty hlavní knihy a prognózy** ke kontrole fronty všech nepotvrzených nákupních objednávek s varováními a chybami kontroly rozpočtu. Pokud má správce rozpočtu nakonfigurovaná oprávnění překročit rozpočet, může potvrdit nákupní objednávky přímo v tomto pracovním prostoru.    

