---
title: Přehled správy funkcí
description: V tomto tématu je popsána funkce správy funkcí a její použití.
author: mikefalkner
manager: AnnBe
ms.date: 09/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: a9be51c4a5cdadd968de160dc0b1406c95382eeb
ms.sourcegitcommit: 260a820038c29f712e8f1483cca9315b6dd3df55
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778698"
---
# <a name="feature-management-overview"></a>Přehled správy funkcí

[!include [banner](../../includes/banner.md)]

Funkce se přidávají a aktualizují v každém vydání. Rozhraní Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.

## <a name="the-feature-management-workspace"></a>Pracovní prostor Správa funkcí

Pracovní prostor **Správa funkcí** lze otevřít výběrem příslušné dlaždice na řídicím panelu. Zobrazí se stránka se seznamem funkcí pro všechny verze, které jsou podporovány rozhraním správy funkcí. V průběhu času společnost Microsoft rozšíří rozhraní správy funkcí tak, aby obsahovalo další funkce, které vám pomohou při správě funkcí.

Seznam funkcí obsahuje následující informace:

- **Název funkce** – Popis přidané funkce.
- **Stav Povoleno** – symbol označuje, zda byla funkce zapnutá (zaškrtnutí), nebyla zapnutá (prázdné pole), byla naplánována pro zapnutí (hodiny), je povinně zapnutá (zámek), vyžaduje pozornost před zapnutím (upozornění), nebo ji nelze povolit (X). Nastavení, které je zobrazeno, je použito pro všechny právnické osoby. Všimněte si, že i když byla funkce zapnuta, je stále řízena zabezpečením. Tato funkce bude proto k dispozici pouze pro uživatele, kteří k ní mají přístup, na základě své role zabezpečení. Bude také k dispozici pouze v právnických osobách, ke kterým má uživatel přístup.
- **Datum povolení** – datum, kdy byla funkce zapnuta nebo na kdy je naplánováno zapnutí.
- **Přidaná funkce** – Datum, kdy byla funkce přidána do vašeho prostředí. Toto datum je automaticky zadáno při aktualizaci prostředí během měsíčního vydání verze.
- **Modul** – Modul, který je touto novou funkcí ovlivněn.

Vyberete-li funkci, zobrazí se v podokně podrobností vpravo od seznamu funkcí další informace. V horní části podokna se zobrazí název funkce, datum, kdy byla funkce přidána, modul ovlivněný funkcí a odkaz na **Další informace**. Tento odkaz vyberte, chcete-li zobrazit dokumentaci k dané funkci. Není-li dokumentace k dispozici, budete navedeni na dočasnou stránku. Podokno podrobností rovněž obsahuje pole **Komentáře**, do kterého můžete přidat vlastní komentáře k funkci.

V pracovním prostoru **Správa funkcí** je také k dispozici několik karet, z nichž každá ukazuje seznam funkcí.

- **Nové** - Na této kartě se zobrazují všechny funkce, které byly přidány od poslední měsíční aktualizace. Pokud jste přeskočili všechny měsíční aktualizace, na kartě se zobrazí všechny nové funkce, které byly přidány od poslední aktualizace. Nejnovější funkce se zobrazí na začátku seznamu. Celkový počet nových funkcí je zobrazen také na dlaždici v horní části stránky.
- **Není povoleno** – na této kartě jsou zobrazeny všechny funkce, které nebyly zapnuty. Nejnovější funkce se zobrazí na začátku seznamu. Celkový počet nových funkcí, které nebyly zapnut,y je uveden také v dlaždici v horní části stránky.
- **Plánováno** – na této kartě se zobrazí všechny funkce, jejichž zapnutí je naplánováno k budoucímu datu. Funkce s nejdřívějším plánovaným datem se zobrazí na začátku seznamu. Celkový počet naplánovaných nových funkcí je zobrazen také na dlaždici v horní části stránky.
- **Vše** – na této kartě jsou zobrazeny všechny funkce. Nejnovější funkce se zobrazí na začátku seznamu.

## <a name="turn-on-a-feature"></a>Zapnutí funkce

Není-li funkce zapnutá, zobrazí se v podokně podrobností tlačítko **Povolit nyní**. Pomocí tohoto tlačítka můžete funkci zapnout.

- Vyberte funkci, kterou chcete zapnout, a poté v podokně podrobností vyberte možnost **Povolit nyní.** Funkce se zapne.

Některé funkce nelze po zapnutí vypnout. Pokud nelze vypnout funkci, kterou se pokoušíte zapnout, zobrazí se upozornění. V tomto okamžiku můžete vybrat možnost **Zrušit**, chcete-li operaci zrušit a ponechat funkci vypnutou. Pokud však vyberete možnost **Povolit** a povolíte funkci, nebude možné ji později vypnout.

Před zapnutím některých funkcí se zobrazí zpráva, která obsahuje další informace. Tyto funkce jsou označeny symbolem žlutého upozornění. Pozorně si přečtěte další informace, abyste lépe pochopili, co se stane, když je funkce povolena. Chcete-li však funkci zapnout, můžete také vybrat možnost **Povolit**.

Některé funkce zobrazí zprávu, že funkci lze povolit až po provedení akce. Tyto funkce jsou označeny symbolem červeného X. Před povolením funkce je nutné podniknout akce popsané v popisu. Pokud například nemůžete použít funkci, dokud není zakázán konfigurační klíč, je nutné nejprve zakázat konfigurační klíč a potom se vrátit ke správě funkcí a povolit tak funkci.

Po zapnutí funkce se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. Tato zpráva buď uvádí, že funkce byla zapnutá, nebo uvádí budoucí datum, na kdy je naplánováno zapnutí funkce. Zobrazí se při každém výběru funkce v seznamu funkcí.

Funkce, jejichž zapnutí je plánováno v budoucnu, se zobrazí na kartě **Naplánované**. Dávkové zpracování je zapne o půlnoci k určitému datu na základě časového pásma, které je vyjádřeno systémovým datem.

## <a name="reschedule-a-feature"></a>Přeplánování funkce

Je-li funkce naplánována na zapnutí v budoucnu, zobrazí se v podokně podrobností tlačítko **Plán**. Toto tlačítko lze použít ke změně hodnoty **Datum povolení** na jiné datum.

1. Vyberte naplánovanou funkci, kterou chcete přeplánovat, a poté v podokně podrobností vyberte možnost **Plán**.
2. V dialogovém okně, které se zobrazí, v poli **Datum povolení** zadejte nové datum, kdy má být funkce zapnuta.
3. Výběrem možnosti **Povolit** přeplánujte funkci nebo volbou **Zakázat** zrušte plán.

## <a name="turn-off-a-feature"></a>Vypnutí funkce

Pokud již byla funkce zapnutá, zobrazí se v podokně podrobností tlačítko **Zakázat**. Pomocí tohoto tlačítka můžete funkci vypnout. Tlačítko **Zakázat** není k dispozici, pokud po zapnutí nejde funkci vypnout.

- Vyberte funkci, kterou chcete vypnout, a poté v podokně podrobností vyberte možnost **Zakázat.** Funkce je vypnutá a pole **Datum povolení** je vymazáno.

Po vypnutí funkce se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. V této zprávě je uvedeno, že funkce ještě nebyla zapnuta. Zobrazí se při každém výběru funkce v seznamu funkcí. Funkce, které nejsou zapnuté, jsou uvedeny na kartě **Není povoleno**.

## <a name="features-that-must-be-turned-on"></a>Funkce, které musí být zapnuté

Někdy je doručena kritická funkce, která musí být povolena automaticky při provedení aktualizace. Tyto funkce budou automaticky zapnuty k datu, které je uvedeno v poli **Datum povolení**. Po povolení těchto funkcí se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. Tato zpráva buď uvádí, že funkce byla zapnutá, nebo uvádí budoucí datum, na kdy je naplánováno zapnutí funkce. Zobrazí se při každém výběru funkce v seznamu funkcí.

## <a name="enable-all-features"></a>Povolení všech funkcí

Ve výchozím nastavení jsou všechny funkce přidané do vašeho prostředí vypnuty. Chcete-li povolit všechny funkce, zvolte tlačítko **Povolit vše**. 

Vyberete-li možnost **Povolit vše**, zobrazí se možnost, kde je třeba zadat následující informace:
- Seznam všech funkcí, které vyžadují potvrzení před tím, než mohou být povoleny. Chcete-li povolit funkce v seznamu, vyberte možnost **Ano** pro tlačítko **Povolit funkce vyžadující potvrzení**.
- Zobrazí se seznam všech funkcí, které nelze povolit. Tyto funkce nebudou povoleny.

Budou povoleny všechny funkce, které lze povolit. Pokud je již v budoucnu naplánováno povolení funkce, plán se nezmění. 

## <a name="turn-on-all-features-automatically"></a>Automaticky zapnout všechny funkce

Ve výchozím nastavení jsou všechny funkce přidané do vašeho prostředí vypnuty, pokud nejsou povinné. Chcete-li však automaticky zapnout všechny nové funkce, můžete pomocí rozevíracího seznamu pod názvem pracovního prostoru změnit, k čemu dojde při přidání nových funkcí.

- Výběrem možnosti **Automaticky povolovat nové funkce** se při přidání do vašeho prostředí automaticky zapnou všechny nové funkce.
- Výběrem možnosti **Automaticky nepovolovat nové funkce** se při přidání do vašeho prostředí automaticky vypnou všechny nové funkce.


Pokud povolíte všechny funkce automaticky, budou zapnuty všechny funkce, které by byly povoleny při kliknutí na tlačítko **Povolit vše**. Nepovolí se funkce vyžadující potvrzení nebo funkce, které nelze povolit, dokud nebude provedena akce.

## <a name="check-for-updates"></a>Zkontrolovat aktualizace

Funkce jsou přidány do vašeho prostředí po každé aktualizaci. Aktualizace však můžete zkontrolovat ručně kliknutím na tlačítko **Vyhledat aktualizace**. Všechny funkce, které byly přidány do systému po aktualizaci, budou přidány do seznamu funkcí. Pokud je například po uvolnění aktivována testovací funkce, můžete vyhledat aktualizace a funkce bude přidána do seznamu.

## <a name="assigning-roles"></a>Přiřazení rolí

Pracovní prostor **Správa funkcí** mohou otevřít správci systému a také uživatelé, kteří jsou přiřazeni k rolím Správce funkcí nebo prohlížečům funkcí, které byly vytvořeny za účelem podpory rozhraní správy funkcí. Tyto dvě role byly vytvořeny za účelem podpory správy funkcí. Uživatelé v roli správce funkcí mohou zapnout nebo vypnout libovolnou funkci. Mohou také aktualizovat pole **Komentáře** pro funkci. Uživatelé v roli prohlížeče funkcí mohou zobrazit pouze pracovní prostor **Správa funkcí**. Nemohou zapínat a vypínat funkce.

Role správce funkcí a prohlížeče funkcí nepřepisují existující zabezpečení, které má uživatel. Pouze ovládají možnost zapnutí a vypnutí funkcí. Neposkytují přístup k funkcím samotným.

## <a name="features-that-use-configuration-keys"></a>Funkce, které používají konfigurační klíče

Pokud funkce používá konfigurační klíč, ale konfigurační klíč není zapnutý, pracovní prostor **Správa funkcí** nezobrazuje funkci v seznamu dostupných funkcí. Po zapnutí konfiguračního klíče je nutné aktualizovat seznam funkcí pomocí položky nabídky **Zkontrolovat aktualizaci**. Funkce se poté zobrazí v seznamu funkcí.

Pokud konfigurační klíč vypnete, funkce nebude ze seznamu funkcí odebrána.

## <a name="data-entities"></a>Datové entity

Datová entita, která je nazvaná **Správa funkcí**, umožňuje exportovat nastavení správy funkcí z jednoho prostředí a poté je importovat do jiného prostředí. Tato entita aktualizuje pouze existující funkce. Obchodní logika v entitě také pomáhá zaručit, že při importu budou použita stejná pravidla, která se používají v pracovním prostoru **Správa funkcí**. Například nelze přepsat povinné nastavení funkce odebráním data během importu.

Následující příklady popisují, co se děje při importu dat pomocí entity **Správa funkcí**.

- Pokud změníte hodnotu pole **Povoleno** na **Ano**, funkce se zapne a v poli **Datum povolení** se nastaví aktuální datum.
- Pokud změníte hodnotu pole **Povoleno** na **Ne** nebo bude v poli **EnableDate** prázdná hodnota, funkce se vypne a pole **Datum povolení** se vymaže. Nelze vypnout povinnou funkci nebo funkci, kterou po zapnutí nelze vypnout.
- Změníte-li hodnotu pole **EnableDate** na budoucí datum, bude pro toto datum naplánována funkce.
- Pokud změníte hodnotu pole **Povoleno** na **Ano** a změníte hodnotu v poli **Datum povolení** na budoucí datum, funkce se naplánuje na toto datum. 
- Pokud změníte hodnotu pole **Povoleno** na **Ne**, ale změníte také hodnotu v poli **Datum povolení** na budoucí datum, funkce se naplánuje na toto datum.
- Je-li funkce zapnuta a přidáte-li pole **EnableDate**, které je nastaveno na budoucí datum, funkce zůstane zapnutá. Chcete-li přeplánovat funkci, musíte změnit pole **Povoleno** na hodnotu **Ne**.

## <a name="feature-management-and-flighting"></a>Správa funkcí a testovací funkce

Správa funkcí vám umožňuje ovládat funkce dodávané v jednotlivých verzích. Testovací verze umožňuje týmům společnosti Microsoft vydávat funkce omezenému počtu zákazníků tak, aby bylo možné funkce testovat a ověřovat bez ovlivnění všech odběratelů. Správa funkcí neřídí testovací verze žádných funkcí.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Použití správy funkcí k zapnutí funkcí ISV nebo vlastních funkcí

Správa funkcí není aktuálně k dispozici pro funkce od nezávislých dodavatelů softwaru (ISV) a vlastních funkcí. Společnost Microsoft však přidává k vylepšení správy funkcí více funkcí. Po dokončení těchto zdokonalení společnost Microsoft zpřístupní správu funkcí pro všechny funkce a poskytne pokyny k aktualizaci funkcí, které chcete použít.
