---
title: Přehled správy funkcí
description: V tomto tématu je popsána funkce správy funkcí a její použití.
author: Peakerbl
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 9b51e848a965589ef0a14e5b880f213d18abc53097c18eed51320d7443a3b5f0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741601"
---
# <a name="feature-management-overview"></a>Přehled správy funkcí

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Funkce se přidávají a aktualizují v každém vydání. Rozhraní Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních. Pracovní prostor pak můžete použít k zobrazení dokumentace funkcí a k povolení nebo zakázání funkcí.

## <a name="the-feature-management-workspace"></a>Pracovní prostor Správa funkcí

Pracovní prostor **Správa funkcí** lze otevřít výběrem příslušné dlaždice na řídicím panelu. Zobrazí se stránka se seznamem funkcí pro všechny verze, které jsou podporovány rozhraním správy funkcí. 

Seznam funkcí obsahuje následující informace:

- **Název funkce** – Popis přidané funkce.
- **Stav** – Symbol označuje, zda je funkce zapnutá (zaškrtnutí), vypnutá (prázdné pole), je naplánována pro zapnutí (hodiny), je povinná (zámek), vyžaduje pozornost před zapnutím (symbol upozornění), nebo ji nelze zapnout (X). Nastavení, které je zobrazeno, je použito pro všechny právnické osoby. Všimněte si, že i když byla funkce zapnuta, je stále řízena zabezpečením. Tato funkce bude proto k dispozici pouze pro uživatele, kteří k ní mají přístup, na základě své role zabezpečení. Bude také k dispozici pouze v právnických osobách, ke kterým má uživatel přístup.
- **Datum povolení** – datum, kdy byla funkce zapnuta nebo na kdy je naplánováno zapnutí.
- **Přidaná funkce** – Datum, kdy byla funkce přidána do vašeho prostředí. Toto datum je automaticky zadáno při aktualizaci prostředí během měsíčního vydání verze.
- **Stav funkce** - Aktuální stav životního cyklu funkce: **Preview**, **Vydáno** (zobrazeno jako prázdné), **Ve výchozím nastavení zapnuto** a **Povinné**. Stavy jsou podrobněji popsány dále v tomto tématu. 
- **Modul** – Modul, který je touto novou funkcí ovlivněn.

> [!NOTE]
> Sloupe **Stav funkce** je zahrnut od verze 10.0.21.

Vyberete-li funkci, zobrazí se v podokně podrobností vpravo od seznamu funkcí další informace. V horní části podokna se zobrazí název funkce, datum, kdy byla funkce přidána, modul ovlivněný funkcí a odkaz na **Další informace**. Tento odkaz vyberte, chcete-li zobrazit dokumentaci k dané funkci. Není-li dokumentace k dispozici, budete navedeni na dočasnou stránku. Podokno podrobností rovněž obsahuje pole **Komentáře**, do kterého můžete přidat vlastní komentáře k funkci.

V pracovním prostoru **Správa funkcí** je také k dispozici několik karet, z nichž každá ukazuje seznam funkcí.

- **Nové** - Na této kartě se zobrazují všechny funkce, které byly přidány od poslední měsíční aktualizace. Pokud jste přeskočili všechny měsíční aktualizace, na kartě se zobrazí všechny nové funkce, které byly přidány od poslední aktualizace. Nejnovější funkce se zobrazí na začátku seznamu. Celkový počet nových funkcí je zobrazen také na dlaždici v horní části stránky.
- **Není povoleno** – na této kartě jsou zobrazeny všechny funkce, které nejsou zapnuty. Nejnovější funkce se zobrazí na začátku seznamu. Kromě toho dlaždice v horní části stránky zobrazuje celkový počet nových funkcí, které jsou aktuálně vypnuté.
- **Plánováno** – na této kartě se zobrazí všechny funkce, jejichž zapnutí je naplánováno k budoucímu datu. Funkce s nejdřívějším plánovaným datem se zobrazí na začátku seznamu. Kromě toho se na dlaždici v horní části stránky zobrazí celkový počet naplánovaných funkcí.
- **Vše** – na této kartě jsou zobrazeny všechny funkce. Nejnovější funkce se zobrazí na začátku seznamu.

## <a name="feature-states"></a>Stavy funkcí
Funkce se mohou přepínat mezi několika stavy, od zavedení ve správě funkcí až po případnou nutnou přítomnost v produktu. Tato část popisuje platné stavy funkcí.

### <a name="preview-features-optional"></a>Funkce Preview (nepovinné)

Produktové týmy se mohou rozhodnout nejprve spustit novou funkci jako funkci preview. Funkce preview nejsou ve výchozím nastavení povoleny a jsou volitelné. Vlastnící produktový tým bude aktualizovat funkce, které budou vydány po dokončení úspěšného období preview.

> [!NOTE]
> Funkce preview podléhají [smluvním podmínkám](https://go.microsoft.com/fwlink/?linkid=2105274) pro konkrétní preview. 

### <a name="released-features-optional"></a>Vydané funkce (volitelné)

Sloupec **Stav funkce** je pro tyto funkce prázdný. Funkce, které jsou původně přidány jako vydané, nejsou ve výchozím nastavení zapnuty a jejich povolení je volitelné. Funkce, které jsou aktualizovány z preview, si zachovají svůj stav povolení.

### <a name="on-by-default-features-optional"></a>Ve výchozím nastavení zapnuté funkce (volitelné)

Funkce, které jsou aktualizovány na hodnotu **Ve výchozím nastavení zapnuto** jsou ve výchozím nastavení zapnuté, ale lze je zakázat. Když se funkce, které lze zakázat, nacházejí ve stavu **Vydáno** po dobu nejméně šesti měsíců, očekává se, že se do tohoto stavu přesunou v příštím hlavním vydání. U funkcí, které přecházejí do stavu **Ve výchozím nastavení zapnuto**, se očekává, že budou uvedeny v části [Co je nového](../whats-new-changed.md) pro dané vydání. Aktualizaci zahájí vlastnící produktový tým.

> [!NOTE]
> Protože tyto funkce budou povoleny automaticky, je důležité určit, zda je vaše organizace připravena tyto funkce převzít, nebo zda potřebujete více času. Pokud je zapotřebí více času, může být nutné dočasně tyto funkce zakázat. Všimněte si, že přechod funkce do stavu **Ve výchozím nastavení zapnuto** se obvykle provádí v hlavním vydání, než se má funkce dostat do stavu **Povinné**. Pak již nebudete mít možnost tuto funkci zakázat. 

### <a name="released-features-mandatory"></a>Vydané funkce (povinné)

**Vydáno** je konečný stav funkcí. Udává, že funkce jsou zapnuté a že je nelze zakázat, aniž byste kontaktovali společnost Microsoft. Očekává se, že volitelné funkce se stanou povinnými po dvou hlavních vydáních. Kriticky důležité funkce mohou být výjimečně zavedeny již jako povinné.

## <a name="example-of-expected-feature-lifecycles"></a>Příklad očekávaných životních cyklů funkcí

Očekává se, že funkce, které lze zakázat a které byly přidány jako vydané a volitelné před nebo jako součást dubnového vydání, přejdou v následujícím říjnovém vydání do stavu **Ve výchozím nastavení zapnuto**. V dubnu následujícího roku se pak očekává, že začnou být **Povinné** .

Očekává se, že funkce, které nelze zakázat a které byly přidány jako vydané a volitelné před nebo jako součást dubnového vydání, přejdou v dubnu příštího roku do stavu **Povinné**.

## <a name="enable-a-feature"></a>Povolení funkce

Není-li funkce zapnutá, zobrazí se v podokně podrobností tlačítko **Povolit nyní**. Pomocí tohoto tlačítka můžete funkci povolit.

Některé funkce nelze po povolení zakázat. Pokud nelze povolit funkci, kterou se pokoušíte zapnout, zobrazí se upozornění. V tomto okamžiku můžete vybrat možnost **Zrušit**, chcete-li operaci zrušit a ponechat funkci zakázanou. Pokud však vyberete možnost **Povolit** a povolíte funkci, nebude možné ji později zakázat.

Před povolením některých funkcí se zobrazí zpráva, která obsahuje další informace. Tyto funkce jsou označeny symbolem žlutého upozornění. Pozorně si přečtěte další informace, abyste měli jistotu, že rozumíte tomu, co se stane po povolení funkce. Chcete-li však funkci povolit, můžete také vybrat možnost **Povolit**.

Některé funkce zobrazí zprávu, že funkci lze povolit až po provedení akce. Tyto funkce jsou označeny symbolem červeného X. Před povolením funkce je nutné podniknout akce popsané v popisu. Pokud například nemůžete použít funkci, dokud není zakázán konfigurační klíč, je nutné nejprve zakázat konfigurační klíč a potom se vrátit ke správě funkcí a povolit tak funkci.

Po povolení funkce se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. Tato zpráva buď uvádí, že funkce byla povolena, nebo uvádí budoucí datum, na kdy je naplánováno povolení funkce. Zobrazí se při každém výběru funkce v seznamu funkcí.

Funkce, jejichž povolení je plánováno v budoucnu, se zobrazí na kartě **Naplánované**. Dávkové zpracování je povolí o půlnoci k určitému datu na základě časového pásma, které je vyjádřeno systémovým datem.

## <a name="reschedule-a-feature"></a>Přeplánování funkce

Je-li povolení funkce naplánováno v budoucnu, zobrazí se v podokně podrobností tlačítko **Plán**. Toto tlačítko lze použít ke změně hodnoty **Datum povolení** na jiné datum.

1. Vyberte naplánovanou funkci, kterou chcete přeplánovat, a poté v podokně podrobností vyberte možnost **Plán**.
2. V dialogovém okně, které se zobrazí, v poli **Datum povolení** zadejte nové datum, kdy má být funkce povolena.
3. Výběrem možnosti **Povolit** přeplánujte funkci nebo volbou **Zakázat** zrušte plán.

## <a name="disable-a-feature"></a>Zákaz funkce

Pokud funkce byla povolena, zobrazí se v podokně podrobností tlačítko **Zakázat**. Pomocí tohoto tlačítka můžete funkci zakázat. Tlačítko **Zakázat** není k dispozici, pokud funkce nemůže být zakázána. 

Po zakázání funkce se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. V této zprávě je uvedeno, že funkce ještě nebyla povolena. Zobrazí se při každém výběru funkce v seznamu funkcí. Funkce, které nejsou povolené, jsou uvedeny na kartě **Není povoleno**.

## <a name="features-that-must-be-enabled"></a>Funkce, které musí být povoleny

Někdy je nasazena kritická funkce, která musí být povolena automaticky při provedení aktualizace. Tyto funkce budou automaticky povoleny k datu, které je uvedeno v poli **Datum povolení**. Po povolení těchto funkcí se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. Tato zpráva buď uvádí, že funkce byla povolena, nebo udává budoucí datum, kdy bude funkce povolena. Zobrazí se při každém výběru funkce v seznamu funkcí.

## <a name="enable-all-features"></a>Povolit všechny funkce

Chcete-li povolit všechny funkce, zvolte tlačítko **Povolit vše**. 

Vyberete-li možnost **Povolit vše**, zobrazí se možnost, kde musíte zadat následující informace:

- Seznam všech funkcí, které vyžadují potvrzení před tím, než mohou být povoleny. Chcete-li povolit funkce v seznamu, vyberte možnost **Ano** pro tlačítko **Povolit funkce vyžadující potvrzení**.
- Zobrazí se seznam všech funkcí, které nelze povolit. Tyto funkce nebudou povoleny.

Budou povoleny všechny funkce, které lze povolit. Pokud je již v budoucnu naplánováno povolení funkce, plán se nezmění. 

## <a name="enable-all-features-automatically"></a>Automatické povolení všech funkcí

Chcete-li automaticky povolit všechny nové funkce, můžete pomocí rozevíracího seznamu pod názvem pracovního prostoru změnit, k čemu dojde při přidání nových funkcí.

- Výběrem možnosti **Automaticky povolovat nové funkce** se při přidání do vašeho prostředí automaticky povolí všechny nové funkce.
- Možnost **Automaticky nepovolovat nové funkce** vyberte, když mají být všechny nové funkce při přidání do vašeho prostředí automaticky vypnuty.

Pokud povolíte všechny funkce automaticky, budou zapnuty všechny funkce, které by byly povoleny při kliknutí na tlačítko **Povolit vše**. Nepovolí se funkce vyžadující potvrzení nebo funkce, které nelze povolit, dokud nebude provedena akce.

## <a name="check-for-updates"></a>Zkontrolovat aktualizace

Funkce jsou přidány do vašeho prostředí po každé aktualizaci. Aktualizace však můžete zkontrolovat ručně kliknutím na tlačítko **Vyhledat aktualizace**. Všechny funkce, které byly přidány do systému po aktualizaci, budou přidány do seznamu funkcí. Pokud je například po uvolnění aktivována testovací funkce, můžete vyhledat aktualizace a funkce bude přidána do seznamu.

## <a name="assigning-roles"></a>Přiřazení rolí

Pracovní prostor **Správa funkcí** mohou otevřít správci systému a také uživatelé, kteří jsou přiřazeni k rolím Správce funkcí nebo prohlížečům funkcí, které byly vytvořeny za účelem podpory rozhraní správy funkcí. Tyto dvě role byly vytvořeny za účelem podpory správy funkcí. Uživatelé v roli správce funkcí mohou zapnout nebo vypnout libovolnou funkci. Mohou také aktualizovat pole **Komentáře** pro funkci. Uživatelé v roli prohlížeče funkcí mohou zobrazit pouze pracovní prostor **Správa funkcí**. Nemohou zapínat a vypínat funkce.

Role správce funkcí a prohlížeče funkcí nepřepisují existující zabezpečení, které má uživatel. Pouze ovládají možnost zapnutí a vypnutí funkcí. Neposkytují přístup k funkcím samotným.

## <a name="features-that-use-configuration-keys"></a>Funkce, které používají konfigurační klíče

Pokud funkce používá konfigurační klíč, ale konfigurační klíč není zapnutý, pracovní prostor **Správa funkcí** nezobrazuje funkci v seznamu dostupných funkcí. Po zapnutí konfiguračního klíče je nutné aktualizovat seznam funkcí pomocí položky nabídky **Zkontrolovat aktualizaci**. Funkce se poté zobrazí v seznamu funkcí.

Pokud konfigurační klíč vypnete, funkce nebude ze seznamu funkcí odebrána.

## <a name="data-entities"></a>Datové entity

Datová entita, která je nazvaná **Správa funkcí**, umožňuje exportovat nastavení správy funkcí z jednoho prostředí a poté je importovat do jiného prostředí. Tato entita aktualizuje pouze existující funkce. Obchodní logika v entitě také pomáhá zaručit, že při importu budou použita stejná pravidla, která se používají v pracovním prostoru **Správa funkcí**. Například nelze přepsat povinné nastavení funkce odebráním data během importu.

Následující příklady popisují, co se děje při importu dat pomocí entity **Správa funkcí**.

- Pokud změníte hodnotu pole **Povoleno** na **Ano**, funkce se povolí a v poli **Datum povolení** se nastaví aktuální datum.
- Pokud změníte hodnotu pole **Povoleno** na **Ne** nebo bude v poli **EnableDate** prázdná hodnota, funkce se zakáže a pole **Datum povolení** se vymaže. Zakázat nemůžete povinnou funkci nebo funkci, kterou po povolení nelze zakázat.
- Změníte-li hodnotu pole **EnableDate** na budoucí datum, bude pro toto datum naplánována funkce.
- Pokud změníte hodnotu pole **Povoleno** na **Ano** a změníte hodnotu v poli **Datum povolení** na budoucí datum, funkce se naplánuje na toto datum. 
- Pokud změníte hodnotu pole **Povoleno** na **Ne**, ale změníte také hodnotu v poli **Datum povolení** na budoucí datum, funkce se naplánuje na toto datum.
- Je-li funkce povolena a přidáte-li pole **EnableDate**, které je nastaveno na budoucí datum, funkce zůstane povolena. Chcete-li přeplánovat funkci, musíte změnit hodnotu pole **Povoleno** na hodnotu **Ne**.

## <a name="feature-management-and-flighting"></a>Správa funkcí a testovací funkce

Správa funkcí vám umožňuje ovládat funkce dodávané v jednotlivých verzích. Testovací verze umožňuje týmům společnosti Microsoft vydávat funkce omezenému počtu zákazníků tak, aby bylo možné funkce testovat a ověřovat bez ovlivnění všech odběratelů. Správa funkcí neřídí testovací verze žádných funkcí.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Použití správy funkcí k zapnutí funkcí ISV nebo vlastních funkcí

Správa funkcí není aktuálně k dispozici pro funkce od nezávislých dodavatelů softwaru (ISV) a vlastních funkcí. Společnost Microsoft však přidává k vylepšení správy funkcí více funkcí. Po dokončení těchto zdokonalení společnost Microsoft zpřístupní správu funkcí pro všechny funkce a poskytne pokyny k aktualizaci funkcí, které chcete použít.

## <a name="frequently-asked-questions-faq"></a>Časté dotazy

### <a name="when-are-features-added-removed-or-changed"></a>Kdy jsou funkce přidány, odebrány nebo změněny? 
Funkce jsou přidávány, odebírány a měněny prostřednictvím změn kódu prováděných vlastnícími produktovými týmy. Prostředí musí být aktualizováno, aby tyto změny přijalo.

### <a name="does-a-feature-become-mandatory-automatically"></a>Stává se funkce povinnou automaticky? 
Ne, funkce se nestane automaticky povinnou. Vlastnící produktový tým musí provést změnu kódu.

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Proč neexistuje konkrétní „povinné povolené datum“? 
Načasování vydání aktualizace je variabilní, načasování aktualizace prostředí je variabilní a zákazníci si mohou vybrat, že některé aktualizace přeskočí. V důsledku toho je obtížné určit konkrétní data. 

### <a name="wheres-the-documentation-for-features-that-are-mandatory"></a>Kde je dokumentace pro povinné funkce? 
Tato dokumentace pochází od každého aplikačního týmu Dynamics 365. Tyto funkce budou často zmíněny v článcích [Aktualizace stavů funkcí klienta](/dynamics365-release-plan/2021wave1/finance-operations/finance-operations-crossapp-capabilities/updates-client-feature-states) nebo [Odebrané nebo zastaralé funkce](../../../dev-itpro/migration-upgrade/deprecated-features.md). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Existuje oznámení v rámci produktu nebo signál, že funkce bude povinně povolena? 
V současné době neexistuje mechanismus oznamování týkající se povinné funkce.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Jsou funkce někdy povoleny, aniž by o tom zákazník věděl? 
Ano, funkce lze povolit bez vědomí zákazníka v následujících situacích:
- Funkce je přesunuta do stavu **Ve výchozím nastavení zapnuto**. V tomto stavu lze tuto funkci stále zakázat. 
- Funkce je aktualizována na stav **Povinné**. Tato změna nastane pouze v kombinaci s hlavní verzí. Kriticky důležité funkce mohou být výjimečně přesunuty do stavu **Povinné** při jakékoli aktualizaci.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Co je to testovací funkce a jak souvisí se správou prvků? 
Testovací funkce jsou přepínače v reálném čase, které řídí společnost Microsoft. Jsou odděleny od zákaznické kontroly poskytované Správou funkcí. 
- Funkce privátní verze Preview nebudou v seznamu správy funkcí uvedeny, dokud nebudou testovány. V provozním prostředí musí zákazník souhlasit, že bude součástí speciálního programu, aby k tomu došlo.
- Funkce ve verzi Public Preview a již vydané (obecně dostupné) funkce budou uvedeny ve Správě funkcí, dokud nebudou otestovány. Testování funkce je pro týmy produktů považováno za poslední možnost, pokud je nalezen kritický problém a obvykle jde o operaci na zákazníka.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Jsou funkce někdy otestovány, aniž by o tom zákazník věděl? 
Ano, pokud funkce ovlivňuje fungování prostředí, které nemá funkční dopad, lze je ve výchozím nastavení povolit.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Jak lze v kódu zkontrolovat povolení funkcí?
Použijte metodu **isFeatureEnabled** na třídu **FeatureStateProvider** a předejte jí instanci třídy funkce. Příklad: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Jak lze v metadatech zkontrolovat povolení funkcí?
Vlastnost **FeatureClass** lze použít k označení, že některá metadata jsou přidružena k funkci. Měl by být použit název třídy použitý pro tuto funkci, například **BatchContentionPreventionFeature**. Tato metadata jsou viditelná pouze v této funkci. Vlastnost **FeatureClass** je k dispozici v nabídkách, položkách nabídek, hodnotách výčtu a polích tabulek / zobrazení.

### <a name="what-is-a-feature-class"></a>Co je třída funkcí?
Funkce ve Správci funkcí jsou definovány jako *třídy funkcí*. Třída funkcí **implementuje IFeatureMetadata** a používá atribut třídy prvků k identifikaci sebe sama v pracovním prostoru Správa funkcí. Existuje mnoho příkladů tříd funkcí, ve kterých lze zkontrolovat povolení v kódu pomocí rozhraní API **FeatureStateProvider** a v metadatech pomocí vlastnosti **FeatureClass**. Příklad: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Co je rozhraní IFeatureLifecycle, které je implementováno některými třídami funkcí?
IFeatureLifecycle je interní mechanismus Microsoftu pro označení fáze životního cyklu funkce. Funkce mohou být tyto:
- `PrivatePreview` – Vyžaduje nasazení testovací verze, aby byla viditelná.
- `PublicPreview` – Zobrazuje se ve výchozím nastavení, ale s upozorněním, že funkce je ve verzi Preview.
- `Released` - Plně uvolněno.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
