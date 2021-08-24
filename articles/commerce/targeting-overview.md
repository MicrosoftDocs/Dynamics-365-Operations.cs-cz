---
title: Cílení na zařízení, trh a geografickou polohu
description: Toto téma popisuje, jak vytvářet, upravovat a spravovat cílové kupiny a cíle v konfigurátoru webů Microsoft Dynamics 365 Commerce pomocí informací o zařízení, trhu a geolokaci.
author: sushma-rao
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 3ecc04c97b42b17f257aa40f665136c70de398748b9bda0da860c7000c062807
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730844"
---
# <a name="device-market-and-geolocation-targeting"></a>Cílení na zařízení, trh a geografickou polohu

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvářet, upravovat a spravovat cílové kupiny a cíle v konfigurátoru webů Microsoft Dynamics 365 Commerce pomocí informací o zařízení, trhu a geolokaci.

Dynamics 365 Commerce umožňuje přizpůsobit variace obsahu vaší stránky (známé jako *cíle*) pro konkrétní skupiny zákazníků (známé jako *cílové skupiny*), které pomohou zvýšit zapojení a spokojenost uživatelů. Nejprve si můžete vytvořit cílovou skupinu nebo cíl. Úspěšné cílení však vyžaduje obě tyto součásti.

V konfigurátoru webů Commerce můžete vytvářet a spravovat cílové skupiny na základě údajů o zákaznících, jako je poloha, informace o zařízení, stav přihlášení a další dynamicky odvozené informace z webových požadavků zákazníků. Můžete také vytvářet a spravovat cíle v modulech a fragmentech elektronického obchodování v konfigurátoru webů Commerce.

**Prohlášení:** Zodpovídáte za používání této funkce v souladu se všemi příslušnými zákony a předpisy, včetně těch, které souvisejí s cílením a profilováním. 

## <a name="audiences"></a>Cílové skupiny

Cílová skupina je skupina uživatelů a členství ve skupině je určeno sadou dynamických pravidel. Tato pravidla jsou jednoduché logické testy, které se spouští proti informacím, které jsou k dispozici v požadavcích zákazníků nebo jiných dostupných segmentech. Můžete kombinovat více pravidel pomocí operátorů AND/OR.

Commerce nativně podporuje základní segmenty, jako jsou informace o zařízení, stav přihlášení, odkazovatel a parametry řetězce dotazu. Podporuje také rozšiřitelné segmenty prostřednictvím připojení k poskytovatelům třetích stran.

### <a name="basic-segments"></a>Základní segmenty

Ve výchozím nastavení jsou k dispozici následující segmenty, které lze zahrnout do definic cílové skupiny:

- **Stav přihlášení** - Otestujte, zda je uživatel ověřen.
- **Platforma zařízení** - Otestujte následující typy zařízení:

    - Mobilní telefon
    - Stolní počítač
    - Tablet
    - Ostatní

- **OS zařízení** - Otestujte následující operační systémy:

    - Windows
    - Linux
    - iOS
    - Android, další

- **Parametry řetězce dotazu** -Otestujte existenci páru klíč – hodnota v parametru řetězce dotazu adresy URL požadavku. Například pro URL `www.fabrikam.com/en-us/request?promo=true` lze napsat pravidlo, které otestuje, že parametr **promo** má hodnotu **true**.
- **Soubor cookie** - Otestujte hodnotu cookie, která je pro doménu nastavena v URL požadavku. Například požadavek Fabrikam.com může obsahovat soubor cookie, který má název **CustomLayout** a hodnotu **1**. Test souborů cookie kontroluje existenci souboru cookie, ale výslovně ho nevytváří. V předchozím příkladu musel JavaScript dříve nastavit soubor cookie **CustomLayout** z jiného modulu nebo jiného obchodního procesu.

    > [!NOTE]
    > Zajistěte, aby vaše používání cookies bylo v souladu s platnými zákony.

- **Odkazovatel** - Pokud uživatel přes odkaz požádá o stránku, je odkazovatelem adresa URL stránky, která odkaz hostovala.

### <a name="extensible-segments"></a>Rozšiřitelné segmenty

Commerce vám umožňuje rozšířit seznam dostupných segmentů připojením k poskytovatelům segmentace třetích stran. Poskytovatel segmentace popíše typy segmentů, které jsou k dispozici. Další informace o tom, jak se připojit k poskytovateli geolokace nebo segmentace, najdete v tématu [Konfigurace a povolení konektorů](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Pokud je povolen externí poskytovatel, může se připojit ke službě, která má nepředvídatelný výkon. Aby byla zajištěna lepší uživatelská zkušenost, pokud uživatel požaduje stránku, která obsahuje cílení, a tato stránka odkazuje na cílovou skupinu, která kontroluje poskytovatele segmentu třetí strany, zobrazí se výchozí verze stránky.
> - Uživatel musí souhlasit s povolením souborů cookies. Prohlížeč uživatele poté požaduje všechny segmenty od příslušných poskytovatelů a výsledky jsou vloženy do souboru cookie, který je vrácen uživateli. Následné požadavky na stránku použijí tyto informace k poskytování cíleného obsahu uživateli. Další informace o dodržování předpisů ohledně souborů cookie naleznete v tématu [Soulad se soubory cookie](cookie-compliance.md).

**Prohlášení:** Pokud tuto funkci povolíte, budou vaše data sdílena se systémy třetích stran, které vyberete. Vy kontrolujete, jaká data, pokud nějaká, poskytnete třetí straně. Berete na vědomí, že standardy zpracování dat a dodržování předpisů třetí stranou se mohou lišit od standardů Microsoft Dynamics 365 Commerce. Vaše soukromí je pro Microsoft důležité. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů a souborech cookie](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Vytvoření cílové skupiny v konfigurátoru webů

Cílovou skupinu vytvoříte v konfigurátoru webů Commerce tímto postupem.

1. V levém navigačním podokně vyberte položku **Cílové skupiny**.
1. Zvolte **Nové**.
1. Zadejte název cílové skupiny. Volitelně můžete také přidat značky a popis.
1. Vyberte **Vytvořit** a pak **Přidat nový blok pravidel**. Blok pravidel je kolekce pravidel, která jsou spojena podmínkami AND. Můžete také vytvořit více bloků pravidel, které mají mezi sebou podmínky OR.
1. Vyberte zdroj dat pro své segmenty a poté zadejte název segmentu, operátor a hodnoty. Můžete vytvořit a odstranit více pravidel v bloku pravidel, nebo můžete vytvořit a odstranit celé bloky pravidel. Bloky pravidel můžete také přesouvat podle potřeby nahoru nebo dolů.

    > [!NOTE]
    > V seznamu můžete mít až 100 hodnot a každá položka seznamu může obsahovat až 50 znaků.

1. Až budete s konfigurací cílové skupiny spokojeni, vyberte **Dokončit úpravy**. Poté můžete vybrat **Publikovat**, aby byla cílová skupina k dispozici pro použití v živém cíli. Alternativně můžete publikovat cílovou skupinu společně s cílem. 

Chcete -li upravit cílovou skupinu, vyberte její hypertextový odkaz na kartě **Cílová skupina** a poté vyberte **Upravit** v editoru cílové skupiny, který se objeví. Chcete -li zobrazit seznam cílů a stránek, které odkazují na cílovou skupinu, vyberte cílovou skupinu v zobrazení seznamu cílových skupin a poté vyberte **Zobrazit přiřazení**. Chcete -li odstranit cílovou skupinu v zobrazení seznamu cílových skupin nebo editoru cílových skupin, zrušte její publikování, pokud již byla publikována, a poté vyberte **Odstranit** na příkazovém řádku.

> [!NOTE]
> Cílové skupiny jsou konceptem na úrovni webu v konfigurátoru webů Commerce. Můžete sdílet stejnou cílovou skupinu ve více cílech.

## <a name="targets"></a>Cíle

Cíl je uživatelské prostředí, které se zobrazuje členům jedné nebo více vybraných cílových skupin. Může zahrnovat variace jednoho nebo více modulů na stránce nebo ve fragmentu. 

Můžete definovat plán pro své cíle a určit, jak dlouho by měly zůstat aktivní. Všimněte si, že tato akce je oddělená od akce plánování skupiny publikování, která určuje, kdy bude publikována kolekce obsahu. Můžete si také prohlédnout náhled svých cílů a zjistit, jak budou vypadat členové vybraných cílových skupin. Kromě toho můžete upřednostnit své cíle a určit, který cíl se má zobrazit v případě konfliktu.

### <a name="create-a-target"></a>Vytvoření cíle

Chcete-li vytvořit prostředí cíle pro moduly stránky v konfigurátoru webů Commerce, postupujte takto.

1. V levém navigačním podokně vyberte položku **Stránky**. Poté vyberte hypertextový odkaz na stránku, která obsahuje moduly, na které chcete cílit.
1. Zvolte **Upravit** pro rezervaci stránky, kterou chcete upravovat.
1. V nabídce **Cíl** vyberte **Nový cíl** k vytvoření nového prostředí cíle. Na stránce můžete vytvořit více cílů podle svých potřeb.
1. Zadejte název a popis svého cíle a vyberte **Další**.
1. Vyberte **Přidat** pro zahrnutí cílových skupin, které uvidí cílený obsah, nebo vyloučení cílových skupin. Pak vyberte **Další**.

    > [!NOTE]
    > Přiřazení cílových skupin je volitelný krok během vytváření cíle. Před publikováním cíle však musíte zahrnout alespoň jednou cílovou skupinu, abyste zajistili, že zamýšlené skupiny uživatelů uvidí cílený obsah.

1. Definujte časové okno pro zobrazení cíle výběrem časového pásma a počátečních a koncových dat a časů. Cíl můžete nastavit tak, aby se zobrazoval vždy během časového okna, nebo můžete vybrat konkrétní dny a časy. Po dokončení zvolte **Další**.

    > [!NOTE]
    > Časy a časové pásmo, které zadáte, jsou globální. Pokud chcete cílit na různá místa v různých časech nebo v různých časových pásmech, musíte vytvořit různé cíle a definovat požadovaný plán pro každé místo.

1. Zkontrolujte podrobnosti a když vše vypadá správně, vyberte **Vytvořit prosředí cíle** a pak **Přejít na cíl**. Vytvoří se prosředí cíle. Nyní do něj můžete přidávat moduly.
1. Vyberte modul, na který chcete cílit, vyberte tři tečky (**...**) a poté vyberte **Přidat k aktuálnímu cíli**. Když cílíte na nadřazený modul, všechny jeho podřízené objekty se stanou součástí tohoto cíle. Cílené moduly jsou zvýrazněny zeleně.
1. Proveďte nezbytné aktualizace obsahu cíleného modulu a podle potřeby přidejte do cíle další moduly. Volbou **Uložit** uložíte všechny své změny.
1. Než publikujete svůj cíl, vyberte **Náhled** na příkazovém řádku a zkontrolujte ho. Poté vyberte jednu z následujících možností:

    - **Základní náhled** - Tuto možnost vyberte, chcete -li zobrazit náhled pouze vybrané varianty (výchozí stránka nebo cíl), bez přidružených cílových skupin.
    - **Rozšířený náhled** - Tuto možnost vyberte, pokud máte na stránce více cílů a chcete si je zobrazit jako uživatel, který patří do vybrané sady cílových skupin, nebo k určitému datu/času. Vyberte **Další** pro výběr ze seznamu relevantních cílových skupin. Můžete také odebrat filtr a vybrat si ze všech cílových skupin.

1. Až budete s cílovou konfigurací spokojeni, musíte stránku publikovat, aby se cíl stal živým. Vyberte **Publikovat**, aby se cíl stal okamžitě živým. Případně můžete k publikování stránky použít naplánovanou skupinu publikování. Informace o skupinách publikování najdete v tématu [Práce se skupinami publikování](publish-groups.md).

Můžete také cílit na fragmenty. Postup je podobný. V kroku 1 však vyberete **Fragmenty** namísto **Stránky** v levém navigačním podokně.

> [!NOTE]
> Abyste se vyhnuli jakémukoli negativnímu dopadu na vaše metriky, můžete mít buď experiment nebo cíle na stránce nebo ve fragmentu. Nemůžete mít experiment a cíle současně.

### <a name="manage-targets"></a>Spravovat cíle

Chcete -li cíle upravit, duplikovat nebo odstranit, přejděte na výchozí stránku nebo fragment a postupujte takto.

1. V rozevírací nabídce vyberte **Cíl** a poté vyberte **Spravovat cíle**.
1. Vyberte cíl, který chcete upravit, duplikovat nebo odstranit.
1. Pokud máte ve stejném modulu více cílů nebo pokud má více cílů konfliktní plány, vyberte **Upřednostnit cíle** a určete pořadí, ve kterém by se měly zobrazovat. Pokud na stránku nebo do fragmentu přidáte více než jeden cíl, na panelu oznámení se také objeví tlačítko **Upřednostnit cíle**, které vám připomene upřednostnění cílů. Není -li zadána žádná priorita, je ve výchozím nastavení vybrán nejnovější cíl.

### <a name="localize-targets"></a>Lokalizace cílů

Cíle na stránkách a ve fragmentech jsou automaticky zahrnuty při exportu a importu souborů XLIFF pro účely lokalizace. Pokud však některá národní prostředí nejsou požadována, můžete pro ně cíle odstranit po importu lokalizovaných souborů XLIFF.

> [!NOTE]
> Cíle jsou spravovány podle kanálu a národního prostředí. Změny, které provedete u cílů v jednom kanálu nebo národním prostředí, nebudou automaticky přeneseny do jiných kanálů nebo národních prostředí.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
