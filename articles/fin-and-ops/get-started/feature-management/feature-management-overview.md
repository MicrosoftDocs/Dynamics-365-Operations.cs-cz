---
title: Přehled správy funkcí
description: V tomto tématu je popsána funkce správy funkcí a její použití.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
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
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538677"
---
# <a name="feature-management-overview"></a>Přehled správy funkcí

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Funkce se přidávají a aktualizují v každém vydání aplikace Microsoft Dynamics 365 for Finance and Operations. Rozhraní Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.

## <a name="the-feature-management-workspace"></a>Pracovní prostor Správa funkcí

Pracovní prostor **Správa funkcí** lze otevřít výběrem příslušné dlaždice na řídicím panelu. Zobrazí se stránka se seznamem funkcí pro všechny verze, které jsou podporovány rozhraním správy funkcí. V průběhu času společnost Microsoft rozšíří rozhraní správy funkcí tak, aby obsahovalo další funkce, které vám pomohou při správě funkcí.

Seznam funkcí obsahuje následující informace:

- **Název funkce** – Popis přidané funkce.
- **Povolený stav** – Symbol označuje, zda byla funkce povolena (zaškrtnutí), není povolena (prázdný), byla naplánována pro povolení (hodiny) nebo je povinně povolená (zámek). Nastavení, které je zobrazeno zde, je použito pro všechny právnické osoby. Všimněte si, že i když byla funkce zapnuta, je stále řízena zabezpečením. Tato funkce bude proto k dispozici pouze pro uživatele, kteří k ní mají přístup, na základě své role zabezpečení. Bude také k dispozici pouze pro právnické osoby, ke kterým má uživatel přístup.
- **Datum povolení** – Datum, kdy byla funkce zapnuta nebo bude zapnuta, pokud je datum v budoucnu.
- **Přidaná funkce** – Datum, kdy byla funkce přidána do vašeho prostředí. Toto datum je automaticky zadáno při aktualizaci prostředí během měsíčního vydání verze.
- **Modul** – Modul, který je touto novou funkcí ovlivněn.

Vyberete-li funkci, zobrazí se v podokně podrobností vpravo od seznamu funkcí další informace. V horní části podokna se zobrazí název funkce, datum, kdy byla funkce přidána, modul ovlivněný funkcí a odkaz na **Další informace**. Tento odkaz vyberte, chcete-li zobrazit dokumentaci k dané funkci. Není-li dokumentace k dispozici, budete navedeni na dočasnou stránku. Podokno podrobností rovněž obsahuje pole **Komentáře**, do kterého můžete přidat vlastní komentáře k funkci.

Pracovní prostor **Správa funkcí** obsahuje také několik karet se seznamem funkcí v něm obsažených. 
- **Nové** -Zobrazí všechny funkce, které byly přidány od poslední měsíční aktualizace. Pokud jste některé měsíční aktualizace přeskočili, bude po poslední aktualizaci obsahovat všechny nové funkce. Nejnovější funkce se zobrazí na začátku seznamu. Celkový počet nových funkcí je zobrazen také na dlaždici v horní části stránky.
- **Nepovoleno** -Zobrazí všechny funkce, které nebyly povoleny. Nejnovější funkce se zobrazí na začátku seznamu. Celkový počet nových funkcí je zobrazen také na dlaždici v horní části stránky.
- **Plánováno** – Zobrazí všechny funkce, které byly naplánovány k povolení k budoucímu datu. Funkce s nejdřívějším plánovaným datem se zobrazí na začátku seznamu. Celkový počet nových funkcí je zobrazen také na dlaždici v horní části stránky.
- **Všechny** -Zobrazí všechny funkce. Nejnovější funkce se zobrazí na začátku seznamu.


## <a name="enable-a-feature"></a>Povolení funkce

Není-li funkce povolena, zobrazí se v podokně podrobností tlačítko **Povolit**. Pomocí tohoto tlačítka můžete funkci povolit.

1. Vyberte funkci, kterou chcete povolit, a poté v podokně podrobností vyberte možnost **Povolit.**
2. Zobrazí se posuvník, kde můžete určit datum, ke kterému by funkce měla být povolena. Ve výchozím nastavení je toto datum nastaveno na aktuální datum.
3. Tuto funkci povolíte výběrem možnosti **Povolit**.

Některé funkce nelze po povolení zakázat. Pokud funkce, kterou se pokoušíte povolit, nemůže být zakázána, zobrazí se upozornění. V tomto okamžiku můžete vybrat možnost **Zrušit**, chcete-li operaci zrušit a ponechat funkci zakázanou. Pokud však vyberete možnost **Povolit** a povolíte funkci, nebude možné ji později zakázat.

Po povolení funkce se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. Tato zpráva buď uvádí, že funkce byla povolena, nebo udává, kdy bude funkce povolena v budoucnu. Pokud použijete budoucí datum, funkce se zobrazí v seznamu **Naplánováno**. Tato zpráva se zobrazí při každém výběru funkce v seznamu funkcí. Funkce naplánované v budoucnu budou povoleny o půlnoci dávkovým procesem založeným na časovém pásmu, které je představováno systémovým datem. 

## <a name="reschedule-a-feature"></a>Přeplánování funkce

Je-li funkce povolena v budoucnu, zobrazí se v podokně podrobností tlačítko **Přeplánovat**. Toto tlačítko lze použít ke změně **data povolení** na jiné datum.

1. Vyberte naplánovanou funkci, kterou chcete přeplánovat, a poté v podokně podrobností vyberte možnost **Přeplánovat**.
2. Zobrazí se posuvník, kde můžete určit datum, ke kterému by funkce měla být povolena. 
3. Výběrem možnosti **Povolit** přeplánujte funkci nebo volbou **Zakázat** zrušte plán.

## <a name="disable-a-feature"></a>Zákaz funkce

Pokud již byla funkce povolena, zobrazí se v podokně podrobností tlačítko **Zakázat**. Pomocí tohoto tlačítka můžete funkci zakázat. Tlačítko **Zakázat** není k dispozici, pokud po povolení nemůže být funkce zakázána.

- Vyberte funkci, kterou chcete vypnout, a poté v podokně podrobností vyberte možnost **Zakázat.**

- Funkce je zakázána a datum je vymazáno.

Po zakázání funkce se pod odkazem **Další informace** v podokně podrobností zobrazí zpráva. V této zprávě je uvedeno, že funkce dosud nebyla povolena, a zobrazí se v seznamu **nepovolených** položek. Tato zpráva se zobrazí při každém výběru funkce v seznamu funkcí.

## <a name="features-that-must-be-enabled"></a>Funkce, které musí být povoleny

Může být doručena kritická funkce, která musí být povolena automaticky při provedení aktualizace. Bude automaticky povolena k **datu povolení**. V podokně podrobností se pod odkazem **Další informace** zobrazí zpráva. Tato zpráva bude uvádět, že funkce byla povolena nebo bude automaticky povolena k **datu povolení**. Zobrazí se při každém výběru funkce v seznamu funkcí.

## <a name="assigning-roles"></a>Přiřazení rolí

Pracovní prostor **Správa funkcí** mohou otevřít správci systému a uživatelé, kteří jsou přiřazeni k rolím Správce funkcí nebo prohlížečům funkcí, které byly vytvořeny za účelem podpory rozhraní správy funkcí. Uživatelé v roli správce funkcí mohou zapnout nebo vypnout libovolnou funkci. Mohou také aktualizovat oddíl komentářů pro funkci. Uživatelé v roli prohlížeče funkcí mohou zobrazit pouze pracovní prostor **Správa funkcí**. Nemohou zapínat a vypínat funkce.

Role správce funkcí a prohlížeče funkcí nepřepisují existující zabezpečení, které má uživatel. Role pouze řídí přístup k povolení funkcí. Neposkytuje přístup k funkcím samotným.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Použití správy funkcí k povolení funkcí ISV nebo vlastních funkcí

Proces správy funkcí není aktuálně k dispozici pro funkce ISV ani pro vlastní funkce. Přidáváme další funkci, která zlepšuje správu funkcí a po dokončení těchto vylepšení otevřeme správu funkcí pro všechny funkce a poskytneme konkrétní pokyny k aktualizaci funkce, aby mohla být použita.

## <a name="feature-management-and-flighting"></a>Správa funkcí a testovací funkce

Správa funkcí vám umožňuje ovládat funkce dodávané v jednotlivých verzích. Testovací verze umožňuje společnosti Microsoft vydávat funkce omezenému počtu zákazníků tak, aby bylo možné funkce testovat a ověřovat bez ovlivnění všech odběratelů. Správa funkcí neřídí testovací verze žádných funkcí.
