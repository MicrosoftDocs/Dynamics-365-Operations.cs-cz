---
title: Přizpůsobte názvy kroků a instrukce pro mobilní aplikaci Warehouse Management
description: Tento článek popisuje, jak vytvořit a zobrazit vlastní pokyny pro každý krok každého toku úkolů, který jste nastavili pro mobilní aplikaci Warehouse Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: faa9bfa320823664603153601c56654170e7e23a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334469"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Přizpůsobte názvy kroků a instrukce pro mobilní aplikaci Warehouse Management

> [!IMPORTANT]
> Funkce, které jsou popsány v tomto článku, platí pouze pro novou mobilní aplikaci Warehouse Management. Nemají vliv na starou skladovou aplikaci, která je nyní zastaralá.

Tento článek popisuje, jak vytvořit a zobrazit vlastní pokyny pro každý krok každého toku úkolů, který jste nastavili pro mobilní aplikaci Warehouse Management. Když skladníci obdrží dobře napsané pokyny, mohou okamžitě začít používat nové toky, aniž by museli předchozí školení. Tato funkce poskytuje následující výhody:

- **Zvyšte rychlost pracovníků tím, že je necháte postupovat podle jednoduchých pokynů pro každý krok úkolu.** Každý krok toku poskytuje pokyny, které umožňují pracovníkům v první linii porozumět úkolu.
- **Poskytněte pokyny, které odpovídají vašim vlastním procesům.** Napište si vlastní pokyny, které budou odpovídat vašim obchodním a skladovým procesům. Například můžete přizpůsobit terminologii vašemu fyzickému prostoru a místním zkratkám.

## <a name="turn-the-warehouse-app-step-instructions-feature-on-or-off"></a>Zapněte nebo vypněte funkci krokových pokynů aplikace Warehouse

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Od verze Supply Chain Management 10.0.29 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.29, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Pokyny ke kroku aplikace skladu* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="step-titles-and-step-instructions-in-the-app"></a>Názvy kroků a pokyny k krokům v aplikaci

Každý krok v toku úkolů v mobilní aplikaci Warehouse Management je identifikován ID kroku. Každý krok má navíc název, ikonu a pokyny. (Další informace viz [Přiřadit ikony a názvy kroků pro mobilní aplikaci Řízení skladu](step-icons-titles.md).)

### <a name="step-titles"></a>Názvy kroků

*Název kroku* je krátký popis toho, co by pracovník měl během kroku dělat. V horní části obrazovky se zobrazí jako velký text, jak ukazuje následující obrázek.

![Příklad názvu kroku v mobilní aplikaci Warehouse Management](media/wma-step-title.png "Příklad názvu kroku v mobilní aplikaci Warehouse Management")

> [!TIP]
> Kvůli velké velikosti textu byste se měli snažit, aby názvy kroků byly co nejkratší. V opačném případě může být text oříznut. U dlouhých názvů však pracovníci mohou stisknutím a podržením názvu otevřít dialogové okno, které zobrazuje celý text.

### <a name="step-instructions"></a>Podrobné pokyny

*Pokyny ke krokům* je delší popis, který poskytuje více informací o tom, co by měl pracovník během kroku udělat. Zobrazí se ve vyskakovacím dialogovém okně, jak ukazuje následující obrázek.

![Příklad pokynů ke kroku v mobilní aplikaci Warehouse Management](media/wma-step-instructions.png "Příklad pokynů ke kroku v mobilní aplikaci Warehouse Management")

Pokyny ke kroku se automaticky zobrazí při otevření kroku. Pracovníci jej mohou odmítnout klepnutím kamkoli mimo vyskakovací dialogové okno. Dialogové okno navíc obsahuje zaškrtávací políčko **Znovu nezobrazovat**, které mohou pracovníci vybrat, aby se zabránilo tomu, že se pokyn objeví při příštím provedení stejného úkolu.

## <a name="load-the-default-setup"></a>Načtěte výchozí nastavení

Když poprvé zapnete *Pokyny ke krokům aplikace Warehouse*, váš systém nebude obsahovat žádné přizpůsobitelné názvy kroků nebo pokyny. První věc, kterou byste měli udělat, je načíst výchozí nastavení. Výchozí nastavení poskytuje texty pro všechna dostupná ID kroků v každém podporovaném jazyce. Chcete-li načíst výchozí nastavení, postupujte takto.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Kroky mobilního zařízení**.
1. V podokně akcí vyberte **Vytvořit výchozí nastavení**. Stránka je vyplněna standardními kroky.

## <a name="customize-step-titles-and-instructions"></a>Přizpůsobte názvy kroků a pokyny

Chcete-li přizpůsobit název a/nebo instrukci pro krok v libovolném počtu jazyků, postupujte takto.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Kroky mobilního zařízení**.

    Stránka **Kroky mobilního zařízení** uvádí všechny kroky, které jsou pro váš systém k dispozici. Každé ID kroku lze sdílet mezi libovolným počtem položek nabídky mobilního zařízení. Pokud je ID kroku sdíleno mezi více položkami nabídky, zobrazí se pro všechny tyto položky nabídky stejný název a instrukce. Můžete však vytvořit přepisy a přizpůsobit tak název a pokyny pro konkrétní položky nabídky. (Další informace naleznete v následující části.)

    Mřížka obsahuje následující sloupce:

    - **Název položky nabídky** - Řádky, kde je tento sloupec prázdný, používají výchozí název kroku a pokyny, které platí pro všechny položky nabídky mobilního zařízení, pro které není definováno žádné přepsání. Řádky, kde je tento sloupec nastaven na název položky nabídky, mají přepisy, které platí pouze pro zadanou položku nabídky.
    - **ID kroku** - Jedinečné ID kroku.
    - **Název pro vstup** - Název, který se zobrazí, když aplikace požaduje nové informace. Pole na stránce jsou obvykle prázdná (to znamená, že nemají žádné přednastavené hodnoty).
    - **Název pro potvrzení** - Název, který se zobrazí, když aplikace požaduje potvrzení hodnoty, která je již v systému uložena. Pole na stránce mají obvykle přednastavené hodnoty.

1. Najděte kombinaci hodnot **ID kroku** a **Názvu položky nabídky**, které chcete upravit, a vyberte hodnotu ve sloupci **ID kroku**. Na stránce, která se otevře, jsou uvedeny všechny dostupné překlady názvu a instrukce vybraného kroku.
1. Podle jednoho z těchto kroků přizpůsobte text pro jakýkoli jazyk. Obě možnosti vám umožňují upravovat texty pro stávající jazyky. Pouze první možnost vám však umožňuje přidat texty pro nové jazyky, zatímco pouze druhá možnost vám umožňuje prohlížet a upravovat texty pro všechny existující přepisy vybraného jazyka specifické pro nabídku.

    - Na panelu nástrojů vyberte **Přidat** a otevřete dialogové okno, kde můžete přidávat nebo upravovat texty pro jakýkoli podporovaný jazyk. Nastavte pole **Referenční jazyk** na jazyk, pro který chcete zobrazit hodnoty. Hodnoty jsou uvedeny v levém sloupci. Nastavte **Jazyk překladů** na jazyk, který chcete přidat nebo upravit. V pravém sloupci upravte hodnoty polí **Název pro vstup**, **Pokyny pro zadání**, **Název pro potvrzení** a **Pokyn k potvrzení** dle potřeby. Pak vyberte **OK**.
    - V mřížce najděte a vyberte řádek, kde je pole **Jazyk** nastaveno na jazyk, který chcete upravit. Na panelu nástrojů vyberte **Zobrazit &lt;jazyk&gt; překladů tohoto kroku** a otevřete dialogové okno, kde můžete upravovat texty pro všechna dostupná přepsání pro vybraný jazyk. Dialogové okno obsahuje mřížku, která obsahuje řádky pro oba standardní texty (kde je pole **Název položky nabídky** prázdné) a u každého dostupného textu přepsání (kde je pole **Název položky nabídky** nastaveno na název položky nabídky, na kterou se vztahuje přepsání). Upravte hodnoty polí **Název pro vstup**, **Pokyny pro zadání**, **Název pro potvrzení** a **Pokyn k potvrzení** dle potřeby. Pak vyberte **OK**.

1. Pokračujte v práci, dokud nedefinujete všechny požadované názvy a pokyny pro každý požadovaný jazyk.

## <a name="add-menu-specific-overrides"></a>Přidejte přepisy specifické pro nabídku

Jak již bylo zmíněno v předchozí části, pro každé ID kroku můžete vytvořit libovolný počet přepsání specifických pro nabídku. Tuto schopnost můžete použít k úpravě a změně pokynů tak, aby lépe odpovídaly vašemu místnímu obchodnímu procesu pro konkrétní položku nabídky. Pokud například při vyskladnění prodejů vaše společnost obvykle poskytuje pracovníkům na vytištěném dokumentu pracovní ID, můžete poskytnout nápovědu, že by pracovníci měli začít naskenováním pracovního ID.

Každé přepsání se vztahuje na konkrétní položku nabídky mobilního zařízení a může obsahovat libovolný počet překladů. Pokud pro položku nabídky neexistuje žádné přepsání, použije položka nabídky standardní texty. Pokud není pro jazyk definován žádný přepisovací překlad, použijí se standardní texty, a to i pro položky nabídky, kde je pro jiné jazyky definováno přepsání.

Chcete-li vytvořit a konfigurovat přepsání, postupujte dle těchto kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Kroky mobilního zařízení**.
1. V mřížce najděte a vyberte řádek, pro který chcete vytvořit přepsání.
1. V podokně akcí vyberte **Přidat konfiguraci kroku**.
1. V rozevíracím dialogovém okně **Přidat konfiguraci kroku** nastavte pole **Položka nabídky** na název položky nabídky mobilního zařízení, na kterou se vztahuje vaše přepsání. Pak vyberte **OK**.
1. Stránka, která se zobrazí, zobrazuje všechny texty, které jsou k dispozici pro nové přepsání. Zpočátku je vytvořen pouze jeden jazyk. Všechny ostatní jazyky budou i nadále používat standardní texty, pokud je sem nepřidáte. Upravte texty a přidejte nové jazyky podle potřeby, jak je popsáno v předchozí části.
