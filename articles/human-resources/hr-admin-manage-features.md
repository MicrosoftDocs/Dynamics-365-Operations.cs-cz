---
title: Správa funkcí
description: Seznamte se s postupy zapnutí a vypnutí nových funkcí v aplikaci Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008325"
---
# <a name="manage-features"></a>Správa funkcí

V rámci našeho průběžného přidávání nových funkcí pro aplikaci Microsoft Dynamics 365 Human Resources chceme, aby zákazníci co nejdříve měli k dispozici nové funkce. Poskytujeme funkce Preview, které jsou téměř připraveny k obecné dostupnosti a prošly rozsáhlým testováním. Právě hledáme další z zpětnou vazbu od zákazníků a ověření před tím, než budou dostupné široké veřejnosti.

Další informace o nových funkcích v Human Resources naleznete v části [Co je nového v Human Resources](hr-admin-whats-new.md) a [plán vydání Dynamics 365 a Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Pracovní prostor **Správa funkcí** uvádí seznam funkcí dodaných v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace. Další informace o aktivaci správy funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru **Správa funkcí** zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.

Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor **Správa funkcí** označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

## <a name="enable-or-disable-preview-features"></a>Povolit nebo zakázat funkce náhledu

Chcete-li získat přístup k funkcím náhledu, je nutné je nejprve povolit ve vašem prostředí. Povolení nebo zakázání funkcí náhledu se vztahuje ke konkrétnímu prostředí.

> [!IMPORTANT]
> Funkce náhledu jsou k dispozici pouze v prostředích **Sandbox**. Když zapnete funkci Preview, povolíte ji pro všechny uživatele ve vaší organizaci, kteří jsou v prostředí. Vypnutím funkce Preview ji zakážete a způsobíte, že budou uživatelům nepřístupné. Funkce Preview mají v aplikaci Human Resources omezenou podporu. Mohou používat méně opatření pro soukromí a bezpečnostních opatření a nejsou zahrnuty do smlouvy o úrovni služeb (SLA) aplikace Human Resources. Neměli byste je používat ke zpracování osobních údajů (to znamená všech informací, které vás mohou identifikovat), nebo ke zpracování jiných dat, které podléhají požadavkům na vyhovění zákonům nebo předpisům.

1. V modulu Human Resources vyberte **Správa systému**.

2. Vyberte dlaždici **Správa funkcí**.

3. Chcete-li povolit funkci Preview, vyberte ji ze seznamu a poté vyberte možnost **Povolit**. Chcete-li zakázat funkci Preview, vyberte ji ze seznamu a poté vyberte možnost **Zakázat**.

## <a name="preview-feature-benefits-management"></a>Funkce Preview: Správa zaměstnaneckých výhod

Správa zaměstnaneckých výhod vám nabízí flexibilní řešení, které podporuje širokou škálu možností zaměstnaneckých výhod spolu se snadno použitelnými zkušenostmi zaměstnanců, které nabízí vaše nabídky. Další informace o konfiguraci a použití správy zaměstnaneckých výhod naleznete v tématu [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).

Správa zaměstnaneckých výhod nahrazuje funkce v pracovním prostoru **Zaměstnanecké výhody**. Pokud povolíte funkci Preview správy zaměstnaneckých výhod, nebude již možné získat přístup k následujícím formulářům v pracovním prostoru **Zaměstnanecké výhody**:

- **Zaměstnanecké výhody**
- **Prvky zaměstnanecké výhody**
- **Sazby pro výpočet příspěvku**
- **Výsledky přihlášení k zaměstnanecké výhodě**
- **Výsledky ukončení nebo prodloužení platnosti zaměstnanecké výhody**
- **Typy pravidel zásad nároků na zaměstnanecké výhody**
- **Zásady způsobilosti k zaměstnaneckým výhodám**
- **Události nároku**

Informace v těchto formulářích lze zobrazit v režimu jen pro čtení. Chcete-li upravit informace, je nejprve nutné zakázat funkci Preview správy zaměstnaneckých výhod.

### <a name="benefits-management-known-issues"></a>Známé problémy se správou zaměstnaneckých výhod

#### <a name="life-events"></a>Životní události

Při zpracování životních událostí se uživateli zobrazí chybová zpráva:

Počáteční datum pokrytí musí být mezi *počátečním obdobím plánu* a *koncem období plánu*. 

Životní událost bude i nadále zpracována očekávaným způsobem.

#### <a name="eligibility-processing"></a>Zpracování posouzení nároku

Při spuštění posouzení nároku na zaměstnanecké výhody, které využívají 1–5násobek platu, % platu a paušální částku krytí, datum podrobností zaměstnaneckých výhod musí být nastaveno na počáteční datum v **Historii zaměstnání**, s odpracovanými hodinami, frekvencí plateb a roční výplatou zaměstnaneckých výhod. Pokud pro pracovníka existuje fixní kompenzace, zadejte odpracované hodiny spolu s frekvencí plateb a bude vypočtena částka roční výplaty. Dostává-li zaměstnanec plat, nemusíte zadávat odpracované hodiny. Doporučujeme, abyste při vytváření nových pracovníků nejprve zadali fixní kompenzaci. Chcete-li aktualizovat záznam o podrobnostech zaměstnaneckých výhod: Přejděte na stránku **Pracovník > Historie pracovníka > Podrobnosti o zaměstnání**. Upravte datum na počáteční datum pracovníka.

#### <a name="employee-self-service"></a>Samoobsluha pro zaměstnance

Zaměstnanci mohou vybrat plán, pro který nejsou kvalifikováni, a rezervovat ho. Například: pracovník nemá žádné rodinné příslušníky, ale může vybrat plán lékařské péče s možností pokrytí rodiny.

Částka zaměstnance se při aktualizaci částky krytí pro životní pojištění nepočítá. Pokud je například zaměstnanci nabídnut plán životního pojištění, může vybrat až 50,000 USD v pokrytí při nákladech 0,36 USD na pokrytí 1 000 USD.  Když zaměstnanec aktualizuje částku pokrytí, přiřazené náklady daného zaměstnance budou nulové.

V případě plánu zaměstnaneckých výhod, který umožňuje pouze jeden výběr tohoto typu plánu, obdrží uživatel při pokusu o odpuštění plánu po výběru plánu chybu. Uživatel například vybere lékařský plán a umístí jej do svého nákupního košíku. Uživatel poté vybere **Vzdát se** pro jiný lékařský plán. Uživateli se zobrazí chybová zpráva.

## <a name="preview-features-in-leave-and-absence"></a>Funkce Preview v pracovním volnu a absenci

Funkce Preview v pracovním volnu a absenci zahrnují:

- **Kalendář pracovního volna a absence** – parametry pracovního volna a absence budou přesunuty z **Parametrů Human Resources** na novou obrazovku nazvanou **Parametry pracovního volna a absence**. Nová obrazovka obsahuje novou kartu **Kalendář**. Tato funkce Preview umožňuje pouze podmnožinu parametrů. K nové obrazovce můžete přistupovat z karty **Odkazy** pracovního prostoru **Pracovní volno a absence**. Kalendáře zahrnují:
  - **Kalendář společnosti** -zobrazí všechny žádosti zaměstnance o volno. Uživatelé s rolí **lidské zdroje** mají k tomuto kalendáři přístup z karty **Odkazy** v pracovním prostoru **Pracovní volno a absence**.
  - **Kalendář týmu manažera** – zobrazí všechny žádosti podřízených o volno. Manažeři mohou získat přístup k kalendáři z karty **Můj tým** ve samoobsluze pro zaměstnance v nabídce **Pracovní volno a absence**. 

- **Kalendáře svátků pracovního vola a absence** – typy volna zahrnují novou možnost **svátků**, která se používá ve spojení s kalendářem pracovní doby. Dny definované svátky a zavíracími dny jsou nyní určeny jako **svátek** při generování pracovních dnů. Při zpracování časového rozlišení jsou úpravy prováděny u zaměstnanců přiřazených ke kalendáři s ohledem na svátky spadající na pracovní den.

- **Audit časového rozlišení pracovního volna** – nová obrazovka umožňuje zkontrolovat, kdy byla časová rozlišení zpracována a odstraněna všemi zaměstnanci i jednotlivými zaměstnanci. K nové obrazovce můžete přistupovat z karty **Odkazy** pracovního prostoru **Pracovní volno a absence**.

- **Odstranění časového rozlišení pracovního volna** – nyní můžete odstranit záznamy časového rozlišení pro konkrétní plány pracovního volna. K nové možnosti můžete přistupovat z karty **Odkazy** pracovního prostoru **Pracovní volno a absence**. U jednotlivých zaměstnanců se tato možnost zobrazí v seskupení **Pracovní volno a absence** v profilu zaměstnance. 

- **Zaokrouhlování časového rozlišení pracovního volna** – nové možnosti pro **Typ pracovního volna** definují, jaký typ zaokrouhlení má časové rozlišení použít, a desetinnou přesnost zaokrouhlení v průběhu procesu časového rozlišení. Při zpracování časových rozlišení jsou zaokrouhlení a přesnost použity pro záznamy časového rozlišení. 

- **Konfigurovat více typů pracovního volna u jednoho plánu pracovního volna** – nový sloupec v plánu časového rozlišení pracovního volna pro typy pracovního volna umožňuje definovat více typů pracovního volna v plánu pracovního volna a absence s různými plány časového rozlišení. Předchozí pole **Typ pracovního volna** je odstraněno. Při registraci zaměstnance se zůstatky pro typy pracovního volna nyní zobrazují v tabulce namísto na horním okraji obrazovky.

  > [!IMPORTANT]
  > Když tuto funkci povolíte, můžete ji poté vypnout.

- **Použití ekvivalentu plného úvazku zaměstnance pro časové rozlišení** – nový sloupec v plánu časového rozlišení pracovního volna pomocí ekvivalentu plného úvazku pro časové rozlišení. Při zpracování časového rozlišení používá aplikace primární pozici zaměstnance a ekvivalent plného úvazku pro určení poměrné částky časového rozlišení.

  > [!NOTE]
  > Tato funkce je k dispozici pouze tehdy, když povolíte možnost **Konfigurovat více typů pracovního volna u jednoho plánu pracovního volna**. 

## <a name="feedback"></a>Zpětná vazba

Rádi bychom se o vás dozvěděli něco o zkušenostech s funkcemi Preview. Doporučujeme vám pravidelně zveřejňovat zpětnou vazbu na následujících webech během používání těchto a dalších funkcí:

- [Komunita](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – tento web je skvělým zdrojem, kde mohou uživatelé diskutovat o případech použití, ptát se a získat nápovědu komunity.
- Dejte nám vědět, jaké funkce chcete zobrazit v produktu nebo o jakýchkoli změnách, které by měly podle vašeho názoru být provedeny u existujících funkcí. Navrhněte nápady týkající se produktů v [nápadech pro Human Resources](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    
Neuvádějte ve zpětné vazbě nebo recenzích na produkty své osobní údaje (některé informace, které by vás mohly identifikovat). Shromážděné informace mohou být dále analyzovány a nebudou použity k odpovídání na žádosti v rámci platných zákonů o ochraně osobních údajů. Osobní údaje, které jsou získány samostatně v rámci těchto programů, se řídí [Prohlášením společnosti Microsoft o ochraně osobních údajů](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Viz také

- [Co je nového v Human Resources](hr-admin-whats-new.md)
- [Plán vydání Dynamics 365 a Power Platform](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)