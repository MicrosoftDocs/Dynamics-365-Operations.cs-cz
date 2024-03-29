---
title: Konfigurace obcházení pro kroky v položkách nabídky mobilního zařízení
description: Tento článek popisuje, jak nakonfigurovat obcházení pro položky nabídky, aby pracovníci mohli zaparkovat aktuální úkol, provést jiný úkol a poté se vrátit k původnímu úkolu bez ztráty jakýchkoli informací.
author: Mirzaab
ms.date: 09/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields, WHSMobileAppFlowStepSelectPromotedFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e387dd4e6499912f2d53dddc17ccc053f1ca699
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689303"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Konfigurace obcházení pro kroky v položkách nabídky mobilního zařízení

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

> [!IMPORTANT]
> Funkce, které jsou popsány v tomto článku, platí pouze pro novou mobilní aplikaci Warehouse Management. Nemají vliv na starou skladovou aplikaci, která je nyní zastaralá.

Tento článek popisuje, jak nakonfigurovat obcházení pro položky nabídky, aby pracovníci mohli „zaparkovat“ aktuální úkol, provést jiný úkol a poté se vrátit k původnímu úkolu bez ztráty jakýchkoli informací.

Obcházení je samostatná položka nabídky, kterou lze otevřít z kroku v hlavním úkolu. Na konci obcházení je pracovník vrácen na místo, kde opustil hlavní úkol. Během konfigurace určíte položku nabídky, která má fungovat jako obcházení. Dále zvolíte, které hodnoty polí z hlavní úlohy se mají automaticky přeposlat (zkopírovat) na obcházení a tam zadat. Proto musíte pochopit, kde v toku úkolů chcete, aby bylo obcházení pro pracovníky dostupné. Musíte také zajistit, aby informace, které je třeba zkopírovat do obcházení, byly pro daný krok postupu úlohy k dispozici.

## <a name="enable-detours-in-your-system"></a>Aktivace obcházení v systému

Než budete moci nakonfigurovat obcházení pro kroky v položkách nabídky mobilního zařízení, musíte provést následující postup, abyste povolili požadované funkce a vygenerovali požadované názvy polí v mobilní aplikaci Warehouse Management.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Ujistěte se, že je funkce *Pokyny pro krok aplikace Warehouse* pro váš systém zapnutá. Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta. Pro více informací o funkci *Pokyny pro krok aplikace Warehouse* viz [Přizpůsobení názvů kroků a pokynů pro mobilní aplikaci Warehouse Management](mobile-app-titles-instructions.md). Tato funkce je předpokladem pro funkci *Obcházení aplikace Warehouse Management*.
1. Zapněte následující funkce, které poskytují funkce popsané v tomto článku:
    - *Obcházení aplikace Warehouse Management*<br>(Od verze Supply Chain Management 10.0.29 je tato funkce ve výchozím nastavení zapnuta.)
    - *Víceúrovňové obcházení pro mobilní aplikaci Warehouse Management*
    - *Automatické odesílání kroků obcházení pro mobilní aplikaci Warehouse Management*
1. Pokud funkce *Obcházení aplikace Warehouse Management* a *Víceúrovňové obcházení pro mobilní aplikaci Warehouse Management* ještě nebyly zapnuty, aktualizujte názvy polí v mobilní aplikaci Warehouse Management tím, že přejdete na **Warehouse Management \> Nastavení \> Mobilní zařízení \> Názvy polí aplikace Warehouse** a vyberete **Vytvořit výchozí nastavení**. Další informace viz [Konfigurace polí pro mobilní aplikaci Řízení skladu](configure-app-field-names-priorities-warehouse.md).
1. Opakujte předchozí krok pro každou právnickou osobu (společnost), kde používáte mobilní aplikaci Warehouse Management.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigurace obcházení z přepsání specifického pro nabídku

Následující postup použijte k nastavení obcházení od přepisu specifického pro nabídku.

1. Vytvořte přepsání specifické pro nabídku pro příslušnou nabídku a krok, jak je popsáno v části [Přizpůsobení názvů kroků a pokynů pro mobilní aplikaci Warehouse Management](mobile-app-titles-instructions.md).
1. Najděte kombinaci hodnot **ID kroku** a **Názvu položky nabídky**, které chcete upravit, a vyberte hodnotu ve sloupci **ID kroku**.
1. Na stránce, která se objeví, na pevné záložce **Dostupná obcházení (položky nabídky)** můžete určit položku nabídky, která by měla fungovat jako obcházení. Dále můžete zvolit, které hodnoty polí z hlavní úlohy se mají automaticky zkopírovat do obcházení a z něj. Příklady, které ukazují, jak tato nastavení používat, naleznete ve scénářích dále v tomto článku.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a><a name="scenario-1"></a>Ukázkový scénář 1: Vychystávání prodeje, kde dotaz na lokalitu funguje jako obcházení

Tento scénář ukazuje, jak nakonfigurovat dotaz na umístění jako obcházení v toku úkolu vychystávání řízeného pracovníky. Toto obcházení umožní pracovníkům vyhledat všechny registrační značky v místě, ze kterého vybírají, a vybrat registrační značku, kterou chtějí použít k dokončení výběru. Tento typ obcházení může být užitečný v případě, že je čárový kód poškozen, a proto je skenerem nečitelný. Případně může být užitečné, když se pracovník musí naučit, co je v systému skutečně k dispozici. Všimněte si, že tento scénář funguje pouze v případě, že vybíráte z míst kontrolovaných registračními značkami.

### <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li použít specifikované ukázkové záznamy a hodnoty k procházení tohoto scénáře, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md). Dříve než začnete, musíte také vybrat právnickou osobu **USMF**.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Vytvoření přepsání specifického pro nabídku a konfigurace obcházení pro scénář 1

V tomto postupu nakonfigurujete obcházení pro položku nabídky **Vyskladnění prodejů** v kroku registrační značky.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Kroky mobilního zařízení**.
1. Najděte pojmenované ID kroku *LicensePlateId* a vyberte ho.
1. V podokně akcí vyberte **Přidat konfiguraci kroku**.
1. V rozevíracím dialogovém okně použijte pole **Položka nabídky** k vyhledání a vybrání *Prodejní vychystávání*.
1. Vyberte **OK**.
1. Zobrazí se stránka podrobností pro přepsání, které jste právě vytvořili. Na pevné záložce **Dostupná obcházení (položky nabídky)** vyberte **Přidat** na panelu nástrojů.
1. V dialogovém okně **Přidat obcházení** vyberte **Dotaz na lokalitu** jako obcházení, které bude zpřístupněno v mobilní aplikaci Warehouse Management.
1. Vyberte **OK**.
1. Na pevné záložce **Dostupná obcházení (položky nabídky)** vyberte obcházení, které jste právě přidali, a poté vyberte **Vybrat pole k odeslání** na panelu nástrojů.
1. V dialogovém okně **Vybrat pole k odeslání** zadejte informace, které mají být odeslány do obcházení a z něj. V tomto scénáři umožňujete pracovníkům používat místo, ze kterého by měli vybírat, jako vstup pro obcházení dotazu na umístění. Proto v části **Odeslání z vychystávání** vyberte **Přidat** na panelu nástrojů pro přidání řádku do mřížky. Poté pro nový řádek nastavte následující hodnoty:

    - **Kopírovat z prodejního vychystávání:** *Umístění*
    - **Vložit do dotazu na umístění:** *Umístění*
    - **Automatické odeslání:** *Vybraný* (stránka bude obnovena s vloženou hodnotou *Umístění*)

1. Vzhledem k tomu, že obcházení je v tomto scénáři nakonfigurováno na kroku registrační značky, bude užitečné, když pracovníci mohou vzít registrační značku z dotazu zpět do hlavního toku. Proto v část **Vzít zpět z dotazu na lokalitu** vyberte **Přidat** na panelu nástrojů pro přidání řádku do mřížky. Poté pro nový řádek nastavte následující hodnoty:

    - **Kopírovat z dotazu na umístění:** *Registrační značka*
    - **Vložit do prodejního vychystávání:** *Registrační značka*
    - **Automatické odeslání:** *Vymazáno* (při návratu z obcházení s hodnotou *Registrační značka* nebude provedena automatická aktualizace)

1. Vyberte **OK**.

Obcházení je nyní plně nakonfigurováno. Tlačítko pro spuštění obcházení **Dotaz na lokalitu** se nyní objeví na kroku registrační značky pro položku nabídky **Prodejní vychystávání**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Dokončete prodejní vychystávání na mobilním zařízení a použijte obcházení

V tomto postupu provedete prodejní vychystávání pomocí mobilní aplikace Warehouse Management. Obcházení, které jste právě nakonfigurovali, použijete k nalezení registrační značky, kterou použijete k provedení kroku vychystávání.

1. V Microsoft Dynamics 365 Supply Chain Management vytvořte prodejní objednávku, která bude vyžadovat krok vyskladnění k odběru z místa, které je sledována registrační značka. Poté vydejte prodejní objednávku do skladu. Poznamenejte si vygenerované ID práce.
1. Otevřete mobilní aplikaci Warehouse Management a přihlaste se do skladu 24. (Ve standardních ukázkových datech se přihlaste pomocí čísla *24* ID uživatele a *1* jako heslo.)
1. Vyberte nabídku **Odchozí** a poté vyberte položku nabídky **Prodejní vychystávání**.
1. Postupujte podle pokynů pro zadávání dat na obrazovce a zadejte ID práce, které bylo vygenerováno v kroku 1.
1. Na kroku, který obsahuje text **Naskenovat registrační značku** otevřete nabídku akcí. Měli byste vidět nové tlačítko označené **Dotaz na lokalitu**. Šipka v levém horním rohu označuje, že tlačítko zahájí obcházení. Vyberte **Dotaz na umístění**.
1. Obcházení je zahájeno. Na další stránce potvrďte umístění, které bylo zkopírováno z hlavního toku.
1. V seznamu dostupných registračních značek v místě klepněte na registrační značku, kterou chcete zkopírovat zpět do hlavního toku. Poté vyberte tlačítko **Zpět**.
1. Vrátíte se zpět do hlavního toku vychystávání prodeje a registrační značka byla zkopírována zpět do něj z obcházení. Potvrďte hodnotu a pokračujte dalším krokem.
1. Nyní můžete provést zbytek standardního toku zadáním požadovaných pokynů pro zadávání dat.

Skladové práce jsou nyní dokončeny. Pracovník úspěšně otevřel obcházení k provedení vedlejšího úkolu (dotazování polohy), aniž by ztratil své místo v hlavním úkolu, a přinesl zpět informace potřebné k provedení hlavního úkolu.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Ukázkový scénář 2: Dotaz na položku s obcházeními pohybu a úpravy

Tento scénář ukazuje, jak nakonfigurovat pohyb a úpravy jako vícenásobná obcházení v toku úlohy dotazování na umístění. Tato schopnost může být užitečná v situacích, kdy pracovník přijede na místo, zjistí, že zásoby v místě se liší od toho, co je evidováno v systému, a proto musí upravit nebo přesunout zboží.

Dotaz na umístění můžete podle potřeby nahradit dotazem na registrační značku nebo dotazem na položku.

### <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li použít specifikované ukázkové záznamy a hodnoty k procházení tohoto scénáře, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/fin-ops/get-started/demo-data.md). Dříve než začnete, musíte také vybrat právnickou osobu **USMF**.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Vytvoření přepsání specifického pro nabídku a konfigurace obcházení pro scénář 2

V tomto postupu nakonfigurujete obcházení pro položku nabídky **Vyskladnění prodejů** v kroku registrační značky.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Kroky mobilního zařízení**.
1. Najděte a vyberte ID kroku s názvem *LocationInquiryList*.

    > [!NOTE]
    > Chcete-li místo dotazu na umístění použít dotaz na položku, vyberte řádek s ID kroku s názvem *ItemInquiryList*. Chcete-li použít dotaz na registrační značku, vyberte řádek ID kroku s názvem *LPInquiryList*.

1. V podokně akcí vyberte **Přidat konfiguraci kroku**.
1. V rozevíracím dialogovém okně použijte pole **Položka nabídky** k vyhledání a vybrání *Dotaz na umístění*.
1. Vyberte **OK**.
1. Zobrazí se stránka podrobností pro přepsání, které jste právě vytvořili. Na pevné záložce **Dostupná obcházení (položky nabídky)** vyberte **Přidat** na panelu nástrojů.
1. V dialogovém okně **Přidat obcházení** vyberte **Pohyb** jako obcházení, které bude zpřístupněno v mobilní aplikaci Warehouse Management.
1. Vyberte **OK**.
1. Na pevné záložce **Dostupná obcházení (položky nabídky)** vyberte obcházení, které jste právě přidali, a poté vyberte **Vybrat pole k odeslání** na panelu nástrojů.
1. V dialogovém okně **Vybrat pole k odeslání** zadejte informace, které mají být odeslány do obcházení a z něj. V tomto scénáři očekáváte, že pracovníci budou hledat místa s řízením registračních značek. Proto bude užitečné zkopírovat registrační značku z dotazu do obcházení **Pohyb**. V části **Odeslání z vychystávání** vyberte **Přidat** na panelu nástrojů pro přidání řádku do mřížky. Poté pro nový řádek nastavte následující hodnoty:

    - **Kopírovat z dotazu na umístění:** *Umístění*
    - **Vložit do pohybu:** *Loc / LP*
    - **Automatické odeslání:** *Vymazáno* (neproběhne žádná automatická aktualizace)

    V tomto obcházení neočekáváte zkopírování žádných informací zpět, protože hlavním tokem byl dotaz, kde nejsou vyžadovány žádné další kroky.

1. Vyberte **OK**.

Obcházení je nyní plně nakonfigurováno. Tlačítko pro spuštění obcházení **Pohyb** se nyní objeví na kroku registrační značky pro položku nabídky **Dotaz na umístění**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Proveďte dotaz na umístěn na mobilním zařízení a použijte obcházení

V tomto postupu provedete dotaz na polohu pomocí mobilní aplikace Warehouse Management. Obcházení pak použijete k provedení pohybu zboží.

1. Otevřete mobilní aplikaci Warehouse Management a přihlaste se do skladu 24. (Ve standardních ukázkových datech se přihlaste pomocí čísla *24* ID uživatele a *1* jako heslo.)
1. Vyberte nabídku **Skladové zásoby** a poté vyberte položku nabídky **Dotaz na umístění**.
1. Zadejte místo, na které se chcete zeptat, např *FL-001*.
1. Když se zobrazí seznam, klepněte a podržte na jedné z karet v něm, abyste zobrazili dostupná obcházení.
1. Vyberte **Pobyb**.
1. Všimněte si, že registrační značka byla zkopírována z karty, kterou jste vybrali. Potvrďte hodnotu.
1. Nyní můžete provést pohyb podle standardního postupu úkolů. Po dokončení práce otevřete nabídku akcí a vyberte **Zrušit**.
1. Jste vráceni na stránku **Dotaz na lokalitu**. Všimněte si, že hodnoty se automaticky neaktualizují. Proto musíte ručně obnovit stránku, abyste viděli změny z obcházení pohybu.

> [!NOTE]
> Funkce *Víceúrovňové obcházení pro mobilní aplikaci Warehouse Management* umožňuje definovat víceúrovňová obcházení (obcházení v rámci obcházení), která umožní pracovníkům přeskočit z existujícího obcházení na druhé a pak zase zpět. Tato funkce ihned podporuje dvě úrovně obcházení a v případě potřeby můžete svůj systém přizpůsobit tak, aby podporoval tři nebo více úrovní obcházení vytvořením rozšíření kódu v tabulce `WHSWorkUserSessionState`.
>
> Funkce *Automatické odeslání kroků obcházení pro mobilní aplikaci Warehouse Management* Tato funkce může pracovníkům urychlit a usnadnit provádění toků obcházení v mobilní aplikaci Warehouse Management. Umožňuje přeskočit některé kroky toku tím, že necháte aplikaci naplnit data obcházení na zadní straně a poté automaticky přejít k dalšímu kroku automatickým odesláním stránky, jak je znázorněno na [*Ukázkový scénář 1: Vychystávání prodeje, kde dotaz na lokalitu funguje jako obcházení*](#scenario-1).
