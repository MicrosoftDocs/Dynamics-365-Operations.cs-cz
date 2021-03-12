---
title: Rozšířené sestavení nákladu během vlny
description: Toto téma uvádí informace o rozšířeném sestavení nákladu během vlny, kdy se automaticky přiřazují dodávky stávajícím vlnám během realizace vlny. Můžete proto vytvářet smysluplné náklady, jež představují kamiony, aniž byste museli používat nástroj pro plánování vytížení.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e4abe1a03997853053f60c750199874a61fc68c0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006384"
---
# <a name="advanced-load-building-during-wave"></a>Rozšířené sestavení nákladu během vlny

[!include [banner](../includes/banner.md)]

Rozšířené sestavení nákladu během vlny přiřazuje automaticky dodávky stávajícím vlnám během realizace vlny. Můžete proto vytvářet smysluplné náklady, jež představují kamiony, aniž byste museli používat nástroj pro plánování vytížení. Tato funkce je užitečná pro firmy, které chtějí používat koncept nákladu ke sledování a plánování přepravy zboží v kamionu či přívěsu, ale nechtějí denně takové náklady vytvářet manuálně.

Během zpracování vlny systém obvykle vytvoří nový náklad pro každou dodávku, ke které není přiřazen žádný náklad. Pokud je však zapnuto pokročilé vytváření nákladů ve vlnách, systém přiřadí každou nepřiřazenou dodávku k existujícímu nákladu (pokud vhodný náklad existuje) a nový náklad se vytvoří, pouze pokud je to požadováno. Rozšířené sestavení nákladu během vlny automaticky vytvoří nové náklady na základě definovaných kritérií.

Chcete-li používat tuto funkci, musíte systém nastavit takto:

- Vytvořte *šablony vlny*, které zahrnují novou metodu **buildLoads**. Tato metoda zpřístupňuje rozšířené sestavení nákladu během vlny pro vlny, které tyto šablony využívají.
- Vytvořte *šablony sestavení nákladu*, každou je třeba propojit s konkrétní šablonou vlny a metodou. Šablony sestavení nákladu řídí, ke kterému nákladu (existujícímu nebo novému) budou přidány řádky nákladu, které jsou zařazovány do vlny. Zásady můžete spojovat nebo rozdělovat dodávky na základě kritérií jako šablona nákladu, vybavení a dalších hodnot polí na řádku nákladu.
- Definujte *skupiny pro spojování nákladů*. S jejich pomocí můžete určovat, které položky lze, případně nelze kombinovat v jednom nákladu. Můžete také určit, zda má omezení vyvolat varování nebo chybu případně zda se má vyhodnocovat objemové omezení šablony nákladu.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Zapnutí funkce Rozšířené sestavení nákladu během vlny v systému

Funkci Rozšířené sestavení nákladu během vlny můžete používat až poté, co ji ve svém systému zapnete. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav těchto funkcí a dle potřeby je zapnout. V pracovním prostoru **Správa funkcí** jsou tyto funkce uvedeny následovně:

- Funkce sestavení nákladu vlny:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *Funkce sestavení nákladu vlny*

- Kód kroků vlny napříč organizací:

    - **Modul:** *Řízení skladu*
    - **Název funkce:** *Kód kroků vlny napříč organizací*

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s touto ukázkou pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tuto ukázku můžete také použít jako vodítko pro použití této funkce při práci na produkčním systému. V takovém případě však musíte nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Ujistěte se, že nastavení scénáře obsahuje dostatečné dostupné zásoby

Pokud pracujete s ukázkovými daty **USMF**, musíte se nejprve ujistit, že je váš systém nastaven tak, aby na každém relevantním skladovém místě bylo k dispozici dost zásob. V rámci této ukázky se očekává, že jsou následující zásoby k dispozici ve skladu *62*:

- **Položka A0001:** 10 ks
- **Položka A0002:** 10 ks
- **Položka M9200:** 10 ks

Položka **M9200** musí být do skladu přidána. Pro přidání zásob položek vykonejte procedury v následujících pododdílech.

#### <a name="create-a-new-license-plate-id"></a>Vytvoření nového ID registrační značky

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Sklad** \> **Registrační značky**.
1. V podokně akcí zvolte **Nový**.
1. V novém řádku zadejte do pole **Registrační značka** hodnotu *LP6203*.
1. Zvolte **Uložit**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Vytvořte standardní náklady pro položku M9200 v lokalitě 6

1. Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.
1. Vyhledejte položku **M9200**.
1. Vyberte řádek s položkou a poté v podokně Akce na kartě **Správa nákladů** vyberte ve skupině **Nastavení** možnost **Cena položky**.
1. Na stránce **Cena položky** vyberte kartu **Nevyřízené ceny**.
1. V podokně akcí zvolte **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Nákladový typ** *Plánované náklady*
    - **Typ ceny:** *Náklady*
    - **Verze:** *10*
    - **Lokalita:** *6*
    - **Cena:** *1,60*

1. V podokně akcí vyberte **Uložit**.
1. V podokně Akce vyberte možnost **Aktivovat nezpracované ceny**.
1. Klikněte na kartu **Aktivní ceny** a ověřte, že byla nová cena pro lokalitu *6* přidána.

#### <a name="create-inventory-in-warehouse-62"></a>Vytvořte zásoby ve skladu 62

1. Přejděte do **Řízení zásob** \> **Položky deníku** \> **Položky** \> **Úprava zásob**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření deníku zásob** vyplňte na záložce s náhledem **Přehled** v poli **Sklad** hodnotu *62*. Potvrďte výchozí hodnoty ve všech ostatních polích.
1. Zvolte **OK** a zavřete dialogové okno.
1. Je otevřena stránka **Úprava zásob**. Na záložce s náhledem **Řádky deníku** vytvořte nový řádek stisknutím tlačítka **Nový**.
1. Na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech ostatních polích.

    - **Číslo položky:** *M9200*
    - **Skladové místo:** *bulk-003*
    - **Množství:** Změňte hodnotu na *10*.

1. V podokně akcí vyberte **Uložit**.
1. Proveďte kontrolu případných chyb v podokně Akce kliknutím na **Ověřit**.
1. V dialogovém okně **Kontrola deníku** spusťte kontrolu stisknutím tlačítka **OK**. Po dokončení kontroly se zobrazí zpráva.
1. V podokně Akce vyberte možnost **Zaúčtovat**. Tím se provede úprava zásob.
1. V dialogovém okně **Zaúčtovat deník** spusťte zaúčtování tlačítkem **OK**. Po provedená zaúčtování se zobrazí zpráva.

## <a name="set-up-advanced-wave-load-building"></a>Nastavení rozšířeného sestavení nákladu během vlny

### <a name="regenerate-wave-process-methods"></a>Obnova metod zpracování vln

Možná bude třeba obnovit metody zpracování vln, abyste měli dostupnou metodu sestavení nákladu (**buildLoads**).

1. Přejděte do **Řízení skladu** \> **Nastavení** \> **Vlny** \> **Metody zpracování vlny**.
2. Ověřte, že je metoda **buildLoads** v seznamu. Pokud není, vyberte v podokně Akce příkaz **Obnovit metody**, abyste ji přidali.

### <a name="set-up-wave-templates"></a>Nastavení šablon vlny

Chcete-li využít výhody rozšířeného sestavení nákladu během vlny, musíte začlenit metodu **buildLoads** do každé relevantní [šablony vlny](tasks/configure-wave-processing.md).

1. Přejděte do **Řízení skladu** \> **Nastavení** \> **Vlny** \> **Šablony vlny**.
1. Vyberte šablonu vlny.

    Pokud pracujete s ukázkovými daty **USMF**, vyberte šablonu **Výchozí expedice 62**.

1. V podokně Akce vyberte možnost **Upravit**, tím přepnete stránku režimu úprav.
1. Na záložce s náhledem **Metody** v mřížce **Zbývající metody** vyberte metodu **buildLoads**.
1. Tlačítkem s šipkou doprava přesuňte metodu **buildLoads** do mřížky **Vybrané metody**.
1. Chcete-li metodě **buildLoads** přiřadit hodnotu **Kód kroku vlny**, musíte příslušný kód nejprve vytvořit na stránce **Kódy kroků vlny**. Můžete použít libovolnou hodnotu, kterou chcete, ale nezapomeňte si ji poznamenat, protože ji budete později potřebovat znát. Podle následujícího postupu vytvořte kód **WSC2112**:

    1. V řádku metody **buildLoads** klikněte pravým tlačítkem myši na šipku dolů v poli **Kód kroku vlny** a vyberte možnost **Zobrazit podrobnosti**.
    1. Na stránce **Kódy kroků vlny** v podokně Akce vyberte **Nový**.
    1. V poli **Kód kroku vlny** zadejte hodnotu *WSC2112*.
    1. V poli **Popis kroku vlny** zadejte hodnotu *WSC2112*.
    1. V poli **Typ kroku vlny** vyberte hodnotu *Sestavení nákladu*.

1. Zvolte **Uložit** a zavřete stránku.
1. V řádku metody **buildLoads** v poli **Kód kroku vlny** vyberte právě vytvořený kód (**WSC2112**).
1. V podokně akcí vyberte **Uložit**.

> [!NOTE]
> Kódy kroků vlny jsou kódy, které mohou uživatelé nastavit a použít k propojení určitých instancí metod vlny s odpovídajícími šablonami. Tyto šablony zahrnují šablony pro doplnění, vytváření kontejnerů, tisk štítků, sestavení a třídění.
>
> Nejsou-li kódy kroků vlny použity, uživatelé musí zadat volný text, který bude odkazovat na určitou šablonu z instance metody vlny. Volný text je náchylný k chybám, protože uživatelé se musí ujistit, že text kroku vlny, který přidávají pro specifickou metodu vlny v šabloně vlny, přesně odpovídá textu kroku vlny v cílové šabloně.
>
> Kódy kroků vlny pro určitý typ kroku vlny jsou nastaveny na samostatné stránce. Pro každou instanci metody kroku vlny v šabloně vlny, která vyžaduje kód kroku vlny, musí být v rozevíracím seznamu vybrán kód kroku vlny. Výběr v rozevíracím seznamu nahrazuje zadávání volného textu a pomáhá snižovat riziko a dopad lidských chyb. Kódy nastavení se používají k propojení metody kroku vlny v šabloně vlny s cílovou šablonou pro metodu.

### <a name="set-up-load-mix-groups"></a>Nastavení skupin pro spojování nákladů

Skupiny pro spojování nákladů určují pravidla pro typy položek, jež lze kombinovat do jednoho nákladu. Můžete nastavit tolik skupin pro spojování nákladů, kolik potřebujete. Chcete-li použít rozšířené sestavení nákladu během vlny, musíte však mít nejméně jednu. Při vytváření skupiny pro spojování nákladů postupujte takto:

1. Přejděte do **Řízení skladu** \> **Nastavení** \> **Náklad** \> **Skupiny pro spojování nákladů**.
1. V podokně Akce vyberte možnost **Nová** a vytvořte novou skupinu nákladů.
1. V poli **ID skupiny pro spojování nákladů** zadejte název nové skupiny.

    Pokud pracujete s ukázkovými daty **USMF**, nastavte následující hodnoty:

    - **ID skupiny pro spojování nákladů:** *TV*
    - **Popis:** *TV*

1. V podokně Akce vyberte možnost **Uložit**. Tím se zpřístupní záložka s náhledem **Kritéria skupiny pro spojování nákladů**.
1. Na záložce s náhledem **Kritéria skupiny pro spojování nákladů** přidejte nový řádek mřížky kliknutím na **Nový**.
1. V novém řádku nastavte ve všech polích požadované hodnoty. Tyto hodnoty určují skupiny položek, které budou zvažovány pro účely spojování nákladů.

    Pokud pracujete s ukázkovými daty **USMF**, vyberte *TV a video* v poli **Skupina položek**.

1. V podokně Akce vyberte možnost **Uložit**. Tím se zpřístupní záložka s náhledem **Omezení skupiny pro spojování nákladů**.
1. Na záložce s náhledem **Omezení skupiny pro spojování nákladů** přidejte nový řádek mřížky kliknutím na **Nový**.
1. V novém řádku nastavte ve všech polích požadované hodnoty.

    Pokud pracujete s ukázkovými daty **USMF**, nastavte následující hodnoty:

    - **Skupina položek:** *CarAudio*
    - **Akce při sestavování nákladu:** *Omezit* (Tato hodnota zabrání, aby byly položky patřící do skupiny položek **CarAudio** umístěny do stejného nákladu jako položky ze skupiny položek **TV a video**.)

1. Pokračujte v práci s pravidly, dokud nepřidáte všechna kritéria a omezení, jež pro skupinu pro spojování nákladů potřebujete.

Pokud pracujete s ukázkovými daty **USMF**, máte nyní nastavení hotové.

### <a name="set-up-load-build-templates"></a>Nastavení šablon sestavení nákladu

Můžete nastavit tolik šablon sestavení nákladu, kolik potřebujete. Chcete-li použít rozšířené sestavení nákladu během vlny, musíte však mít nejméně jednu. Při vytváření šablony sestavení nákladu postupujte podle těchto kroků.

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Náklad** \> **Šablony sestavení nákladu během vlny**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty.

    | Pole | popis | Hodnota v ukázkových datech USMF |
    |---|---|---|
    | Pořadové číslo | Pořadí, v jakém bude šablona vyhodnocována. | *1* |
    | Název šablony sestavení vytížení | Zadejte jedinečný identifikátor šablony sestavení nákladu. V tomto nastavení byste měli zadat název šablony, kterou jste předtím vytvořili nebo aktualizovali. | *Výchozí expedice 62* |
    | Kód kroku vlny | Zadejte kód kroku vlny k použití pro účely propojení šablony s metodou vlny. Měli byste zadat kód, který jste vybrali pro metodu **buildLoads**, když jste při tomto nastavování předtím vytvářeli šablonu vlny. | *WSC2112* |
    | ID šablony nákladu | Vyberte šablonu nákladu, která se má použít, když se vytvářejí nové náklady, proti které se má párovat při přiřazování ke stávajícím nákladům. Šablona nákladu definuje maximální přípustnou hmotnost a objem celého nákladu. | *Stand. šablona nákladu* |
    | Vybavení | Vybavení, proti kterému má být dosažena shoda při přiřazení ke stávajícím nákladům a pro zadání nových vytvářených nákladů. | Pole ponechejte prázdné. |
    | ID skupiny kombinace vytížení | Vyberte skupinu pro spojování nákladů, jež se má použít, pokud je položka v nákladu povolena. Skupina pro spojování určuje pravidla pro typy položek, jež lze kombinovat do jednoho nákladu. Měli byste vybrat jednu ze skupin pro spojování, které jste vytvořili dříve během tohoto nastavování. | *TV* |
    | Použít otevřená vytížení | Vyberte, zda mají být přidány stávající otevřené náklady. Existují tyto možnosti:<ul><li>**Žádný** – nepřidávat žádné otevřené náklady ke stávajícím nákladům.</li><li>**Jakýkoli** – přidávat otevřené náklady ke stávajícím nákladům, jež jsou pro daný řádek platné.</li><li>**Přiřazený** – přidat otevřené náklady k nákladu, který je přiřazen k vlně.</li></ul> | *Libovolná* |
    | Vytvořit vytížení | Určete, zda by měly být vytvořeny nové náklady, pokud žádné stávající náklady nesplňují zadaná kritéria. | Vybráno (= *Ano*) |
    | Povolit dělení řádků dodávky | Určete, zda může být řádek nákladu dělen na více nákladů, pokud úplný řádek překračuje maximální kapacitu šablony nákladu. | Nezaškrtnuto (= *Ne*) |
    | Ověřit objem | Určete, zda by sestavení nákladu mělo kontrolovat hmotnost při přidání každého řádku nákladu, aby bylo zajištěno, že budou dodrženy volumetrické limity šablony nákladu. | Nezaškrtnuto (= *Ne*) |

1. V podokně Akce zvolte možnost **Uložit**. Tím se zpřístupní možnost **Upravit dotaz**.
1. V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno pro editaci dotazu.
1. V dialogovém okně klikněte na kartu **Třídění** a tlačítkem **Přidat** přidejte řádek mřížky.
1. Na novém řádku definujte pravidla třídění, jež chcete použít. Chcete-li například výsledky řadit vzestupně podle čísla objednávky, nastavte následující hodnoty:

    - **Tabulka:** *Podrobnosti nákladu*
    - **Odvozená tabulka:** *Podrobnosti nákladu*
    - **Pole:** *Číslo objednávky*
    - **Směr hledání:** *Vzestupně*

1. Stiskněte **OK**, uložte změny a zavřete dialogové okno.
1. Na záložce s náhledem **Dělit podle** nastavte pravidla řídící, jak budou náklady děleny. Obvykle můžete dělit podle vlastních polí, jež platí pro řádek nákladu, například **Trasa**, **Prohlídka** nebo **Spuštění**. Chcete-li například vytvořit jeden náklad na číslo objednávky, zaškrtněte políčko **Dělit podle** u řádku, v němž jsou následující hodnoty:

    - **Název referenční tabulky:** *Podrobnosti nákladu*
    - **Název referenčního pole:** *Číslo objednávky*

## <a name="scenario"></a>Scénář

Tento scénář ukazuje, jak nastavení, jež bylo popsáno výše v tomto tématu, ovlivňují skladové operace prováděné při zpracování prodejní objednávky. Tento scénář používá ukázková data **USMF** a další ukázkové hodnoty uvedené v pokynech pro nastavení.

### <a name="create-sales-orders"></a>Vytvářet prodejní objednávky

1. Přejděte na **Prodej a marketing** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.
1. V podokně Akce zvolte možnost **Nová** a otevře se dialogové okno **Vytvoření prodejní objednávky**.
1. V dialogovém okně nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-007*.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *62*.

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Měla by obsahovat nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**. Na tomto novém řádku nastavte v poli **Číslo položky** hodnotu *A0001* a v poli **Množství** hodnotu *1*.
1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži**.
1. Chcete-li se vrátit na prodejní objednávku, zavřete stránku kliknutím na tlačítko **Zavřít** (**X**) v pravém horním rohu stránky.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.** Systém vytvoří dodávku a přidá ji k novému nákladu, protože žádný stávající náklad neobsahuje řádky nákladu s tímto číslem objednávky.

    Zobrazí se informační zprávy určující práci, vlnu a dodávku, jež byly vytvořeny pro tuto objednávku.

1. Chcete-li potvrdit údaje o nákladu, dodávce a práci z řádku prodejní objednávky, vyberte řádek a poté v nabídce **Sklad** nad mřížkou vyberte **Podrobnosti nákladu**, **Podrobnosti dodávky** nebo **Podrobnosti práce**.
1. V prodejní objednávce, kterou jste právě vytvořili, vyberte na záložce s náhledem **Řádky prodejní objednávky** možnost **Přidat řádek**. Přidá se další řádek.
1. Na novém řádku nastavte v poli **Číslo položky** hodnotu *A0002* a v poli **Množství** hodnotu *1*.
1. Opakujte kroky 6 až 9, až provedete rezervaci řádku a uvolněte jej do skladu. Systém vytvoří **novou** dodávku pro přidaný řádek. Protože však používáte rozšířené sestavení nákladu během vlny, přidá systém tuto dodávku a řádek nákladu k existující vlně. Pokud byste nepoužívali rozšířené sestavení nákladu během vlny, systém by pro zásilku vytvořil nový náklad.
1. V prodejní objednávce, kterou jste právě vytvořili, vyberte na záložce s náhledem **Řádky prodejní objednávky** možnost **Přidat řádek**. Přidá se další řádek.
1. Na novém řádku nastavte v poli **Číslo položky** hodnotu *M9200* a v poli **Množství** hodnotu *1*.
1. Opakujte kroky 6 až 9, až provedete rezervaci řádku a uvolněte jej do skladu. Stejně jako předtím, vytvoří systém **novou** dodávku pro přidaný řádek. Protože je však položka ze skupiny položek **CarAudio**, **neprojde přes omezení, která jste nastavili pro skupinu pro spojování nákladů**. Proto se **přidá do nového nákladu**. Pokud jste nezadali skupinu pro spojování nákladů v šabloně sestavení nákladu, byla by tato dodávka přidána k prvnímu nákladu.
