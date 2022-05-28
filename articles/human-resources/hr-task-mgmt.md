---
title: Správa úkolů
description: Toto téma vysvětluje funkce správy úloh, které jsou k dispozici v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae453bd57217f272038decc7e40ed373f618ae03
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710214"
---
# <a name="task-management"></a>Správa úkolů

[!INCLUDE [PEAP](../includes/peap-1.md)]

Správa úkolů vám umožňuje vytvářet úkoly, které je třeba splnit, abyste mohli najmout (nasadit), propustit (rušit) a převádět (přechod) zaměstnance. Řízení úkolů využívá koncept kontrolních seznamů. Kontrolní seznam je seznam úloh nasazování, rušení a přechodu. Správa úkolů používá kontrolní seznamy k seskupování úkolů a k jejich přiřazení jednotlivcům nebo skupinám. Funkce kontrolního seznamu pro nasazování, rušení a přechody jsou podobné.

## <a name="checklist-overview"></a>Přehled kontrolního seznamu

Kontrolní seznam je skupina úkolů. Kontrolní seznamy vám poskytují flexibilní způsob seskupování úkolů a lze je znovu použít (například když najmete další zaměstnance). Můžete vytvořit tolik kontrolních seznamů, kolik potřebujete, a stejné úkoly můžete přiřadit více kontrolním seznamům.

### <a name="examples"></a>Příklad

Následující příklady ukazují, jak lze kontrolní seznamy použít v procesu registrace. Protože je však funkce kontrolního seznamu pro nasazování, rušení a přechody podobná, informace se vztahují také na procesy rušení a přechodu.

V rámci procesu nasazování mohou pracovníci personálního oddělení (HR) vytvářet úkoly, které sledují průběh nasazování příchozích a nedávno přijatých zaměstnanců. Protože se proces nasazování může lišit v závislosti na pozici nebo geografické poloze zaměstnance, můžete vytvořit několik kontrolních seznamů pro nasazování, které vyhovují různým situacím při najímání.

**Příklad 1**

Každý zaměstnanec, který je najat ve Spojených státech, musí splnit úkoly, jako je vyplňování formulářů pro srážkovou daň. Úkoly, jako je přidělení služebního vozidla, se však mohou vztahovat pouze na zaměstnance na vedoucí úrovni. V tomto případě lze vytvořit dva kontrolní seznamy pro registraci: **Zaměstnanci se sídlem v USA** a **Pouze vedoucí úroveň**. Když je pak ve Spojených státech najat manažer na střední úrovni, je vybrán kontrolní seznam **Zaměstnanci se sídlem v USA**. Když je však ve Spojených státech najat vedoucí pracovník, vyberou se oba kontrolní seznamy, aby bylo zajištěno, že budou splněny všechny požadované úkoly spojené s nasazováním.

**Příklad 2**

Společnost má jak sezónní zaměstnance, tak kmenové zaměstnance na plný úvazek. Přestože se některé úkoly (např. ověření času příchodu nového zaměstnance) týkají zaměstnanců obou typů, některé další úkoly se týkají pouze běžných zaměstnanců na plný úvazek. V tomto případě můžete vytvořit dva kontrolní seznamy. Oba kontrolní seznamy obsahují úkoly, které se vztahují na sezónní i běžné zaměstnance na plný úvazek, ale pouze jeden kontrolní seznam obsahuje úkoly, které jsou specifické pro běžné zaměstnance na plný úvazek.

## <a name="task-management-workspace"></a>Pracovní prostor správy úkolu

Pracovní prostor **Správa úkolů** uvádí všechny úkoly, které byly přiřazeny jednotlivcům v procesech nasazování, rušení a přechodu. Chcete-li zobrazit úlohy pro proces, vyberte příslušnou kartu v levém horním rohu: **Nasazování**, **Rušení** nebo **Přechody**. Ve výchozím nastavení mají přístup k pracovnímu prostoru **Správa úkolů** pouze personalisté.

Karta **Nasazování** obsahuje seznam **Brzy začíná**, který zobrazuje příchozí zaměstnance a seznam **Nedávno přijatí zaměstnanci**, který zobrazuje nedávno přijaté zaměstnance. V obou seznamech můžete vybrat pouze jednoho zaměstnance. Když vyberete zaměstnance, na pravé straně stránky se zobrazí všechny úkoly související s nástupem daného zaměstnance. Karta **Nasazování** také obsahuje seznam **Všechny úkoly**, který zobrazuje všechny úkoly pro všechny příchozí nebo nedávno přijaté zaměstnance. Nakonec obsahuje seznam zpožděných úkolů a seznam úkolů, které jsou přiřazeny aktuálnímu uživateli.

Karta **Rušení** záložka obsahuje seznam zaměstnanců, kteří ze společnosti odcházejí, a seznam zaměstnanců, kteří již ze společnosti odešli. V obou seznamech můžete vybrat pouze jednoho zaměstnance. Když vyberete zaměstnance, zobrazí se všechny úkoly související s rušením daného zaměstnance. Karta **Rušení** také obsahuje seznam **Všechny úkoly**, který zobrazuje všechny úkoly pro všechny odcházející nebo minulé zaměstnance. Nakonec obsahuje seznam zpožděných úkolů a seznam úkolů, které jsou přiřazeny aktuálnímu uživateli.

Karta **Přechody** obsahuje seznam **Všechny úkoly**, který zobrazuje všechny úkoly pro všechny zaměstnance, kteří budou měnit pozici nebo kteří nedávno změnili pozici. Existuje také seznam zpožděných úkolů a seznam úkolů, které jsou přiřazeny aktuálnímu uživateli.

Na všech třech kartách mohou HR asistenti a manažeři provádět následující činnosti:
- Aplikace kontrolního seznamu na zaměstnance
- Aktualizace stavu úkolu
- Opětovné přiřazení úkolu
- Aktualizace termínu dokončení úkolu

> [!NOTE]
> Ve výchozím nastavení karta **Nasazování** zobrazuje zaměstnance, kteří byli najati za posledních sedm dní. Chcete-li toto nastavení změnit, na stránce **Parametry lidských zdrojů** na kartě **Všeobecné** v poli **Poslední přijatí** definujte časový rámec. Údaje v seznamu **Poslední přijatí** lze zobrazit pro konkrétní počet dní, měsíců nebo let. Chcete-li například zobrazit seznam zaměstnanců, kteří byli přijati za posledních 14 dní, nastavte pole **Doba** na **14** a pole **Jednotka** na **Dny**.
> Na stránce **Parametry lidských zdrojů** můžete také aktualizovat časové období pro seznamy odcházejících a odešlých zaměstnanců, kteří jsou uvedeni na kartě **Rušení**. Tato nastavení platí také pro pracovní prostor **Správa personálu**.

## <a name="setting-up-tasks"></a>Nastavení úkolů

Úkoly můžete vytvářet jednotlivě a poté je znovu použít ve více kontrolních seznamech. Chcete-li vytvořit úkol, na stránce **Nastavení nasazování** na kartě **Úkoly** vyberte **Nový**.

Případně můžete úkoly přidat přímo do kontrolního seznamu. Chcete-li přidat úkol do kontrolního seznamu, na stránce **Nastavení nasazování** na kartě **Kontrolní seznam** vytvořte nový kontrolní seznam, do kterého chcete úkol přidat, nebo přidejte úkol do existujícího kontrolního seznamu.

> [!NOTE]
> Pokud úkol přidáte přímo do kontrolního seznamu, nemůžete jej znovu použít v jiných kontrolních seznamech.

Následující tabulka popisuje pole, která jsou k dispozici, když vytvoříte úlohu některou z metod.

| Pole           | Popis |
|-----------------|-------------|
| Úkol            | Zadejte název úkolu. |
| Popis     | Zadejte popis úkolu. |
| Volitelné        | Zadejte, zda je úkol volitelný a má pouze informativní charakter. |
| Odkaz na úkol       | Zadejte adresu URL externí webové stránky nebo konkrétní stránky v aplikaci, kde má uživatel úkol provést. Více informací viz část [Odkazy na úkoly](#task-links). |
| Typ přiřazení | Úkoly mohou být přiděleny konkrétnímu pracovníkovi, pozici nebo skupině pozic, vedoucímu dotčeného zaměstnance (tj. zaměstnanci, který je součástí procesu nasazování, rušení nebo přechodu) nebo dotčeného zaměstnance. Vyberte typ přiřazení. Více informací viz část [Typy přiřazení](#assignment-types). |
| Přiřazeno k     | Vyberte konkrétního pracovníka, pozici nebo skupinu pozic, kterým chcete úkol přiřadit. |
| Kontaktní osoba  | Uveďte osobu, která by měla být kontaktována v případě dotazů k úkolu. |
| Posun termínu splnění | Zadejte počet dní před datem nasazení, zrušení nebo přechodu nebo po něm, kdy má úkol splnit. Více informací naleznete v části [Termíny splnění úkolů a pole Posun termínu plnění](#task-due-dates-and-the-due-date-offset-field). |
| Instrukce    | Zadejte pokyny pro provedení úkolu. Další informace naleznete v části [Pokyny](#instructions). |

### <a name="task-links"></a>Odkazy na úkol

Odkaz na úkol poskytuje odkaz na externí webovou stránku nebo stránku v aplikaci Dynamics 365. Pokud má osoba přiřazená k úkolu přejít na konkrétní webovou stránku nebo konkrétní stránku v aplikaci Dynamics 365, aby tento úkol provedla, můžete zadat odkaz na úkol. Když vytvoříte odkaz na úkol, můžete vybrat jednu z následujících možností:

- **Položka nabídky** – Pokud vyberete tuto možnost, zobrazí se seznam všech stránek v aplikaci Dynamics 365. Vyberte stránku v seznamu.
- **URL** – Pokud vyberete tuto možnost, zadejte adresu URL webové stránky, na kterou má přejít osoba přiřazená k úkolu. Zadaná stránka může být stránkou, která není součástí aplikace Dynamics 365.
- **Detaily pracovníka** – Pokud vyberete tuto možnost, vyberte jednu z následujících možností:

    - **Zaměstnanecké samoobslužné akce** – Tato možnost zobrazí seznam stránek, které jsou k dispozici v **Zaměstnanecké samoobsluze**. Použijte jej, pokud úkol, který byl přidělen zaměstnanci na palubě, musí být proveden v **Zaměstnanecké samoobsluze**. Pokud například chcete, aby zaměstnanec zadal své osobní kontaktní údaje, vyberte **Zaměstnanecké samoobslužné akce** a poté vyberte **Osobní údaje&gt;Osobní údaje**.
    - **Akce řízení pracovníků** – Tato možnost zobrazí seznam stránek, které souvisejí se záznamem pracovníka, ale nejsou pro zaměstnance přístupné. Pokud například chcete, aby vlastník úkolu zadal informace, které jsou specifické pro nasazeného pracovníka, jako jsou informace o odměně, vyberte **Akce správy pracovníků** a poté vyberte **Kompenzace&gt;Pevná kompenzace**.

### <a name="assignment-types"></a>Typy přiřazení

Když je zaměstnanec přijat, propuštěn nebo převeden, lze vybrat jeden nebo více kontrolních seznamů. Po výběru kontrolního seznamu a dokončení procesu náboru, propuštění nebo převodu jsou vytvořeny úkoly a přiřazeny uživatelům ke sledování pokroku.

Když je úkol vytvořen, je přiřazen konkrétnímu uživateli. Uživatel, kterému je úkol přiřazen, závisí na typu přiřazení, který je pro daný úkol vybrán. Následující hodnoty jsou k dispozici v poli **Typ přiřazení**:

- **Pracovník** – Přidělte úkol konkrétnímu pracovníkovi. Po výběru této hodnoty vyberte pracovníka v poli **Přiřazený pro**.
- **Pozice** – Přidělte úkol konkrétní pozici. Po výběru této hodnoty vyberte pozice v poli **Přiřazený pro**.

    Například IT technik bude vždy zodpovědný za přípravu notebooku pro nového zaměstnance. V tomto případě, když vytvoříte úkol konfigurace notebooku, vyberte **Pozice** jako typ přiřazení a poté zvolte **Technik IT** jako pozici. Poté, když je přijat zaměstnanec a je přiřazen kontrolní seznam, je úloha konfigurace notebooku přiřazena kterémukoli pracovníkovi, který je v době zadání akce na pozici IT technika.

- **Skupina** – Přidělte úkol skupině pozic (skupina přiřazení). Po výběru této hodnoty vyberte skupinu v poli **Přiřazený pro**. Další informace naleznete v části [Nastavení skupin přiřazení (volitelné)](#setting-up-assignment-groups-optional).
- **Manažer** – Přidělte úkol vedoucímu zaměstnance, který je přijímán, propouštěn nebo převáděn.

    > [!IMPORTANT]
    > Při použití kontrolního seznamu, pokud najatému, propuštěnému nebo převedenému zaměstnanci není aktuálně přiřazena žádná pozice, nelze manažera určit. V tomto případě je úkol přiřazen vlastníkovi kontrolního seznamu. Další informace naleznete v části [Nastavení kontrolních seznamů](#setting-up-checklists).

- **Zaměstnanec** – Přiřaďte zaměstnance, který je přijímán, propouštěn nebo převáděn.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Termíny plnění úkolů a pole Posun termínu plnění

Termíny plnění úkolů vycházejí z data zahájení zaměstnání, data ukončení nebo data přechodu. Některé úkoly musí být provedeny před počátečním datem zaměstnance, zatímco jiné úkoly mohou být provedeny později. Při definování úkolu zadáte v poli **Posun termínu splnění** nastavíte termín splnění, které je relativní k počátečnímu datu, datu propuštění nebo datu přechodu. Například IT technik musí připravit notebook pro nového zaměstnance dva dny před datem nástupu tohoto zaměstnance. V tomto případě, když vytváříte úkol konfigurace notebooku, nastavte **Posun termínu splnění** pole na **−2**. Pak, pokud je datum nástupu zaměstnance 5. května, bude mít úkol termín 3. května.

> [!NOTE]
> Termíny splnění lze upravit také po vytvoření úkolu.

Termíny splnění se počítají na základě kalendáře, který je přidružen ke kontrolnímu seznamu. Další informace naleznete v části [Nastavení kontrolních seznamů](#setting-up-checklists).

### <a name="instructions"></a>Instrukce

Komplexní úkoly mohou vyžadovat více kroků, nebo osoby provádějící úkol musí poskytnout další informace. Do pole **Pokyny** můžete zadat pokyny a další informace, které pomohou osobě, která má úkol dělat, ho splnit.

## <a name="setting-up-checklists"></a>Nastavení kontrolních seznamů

Kontrolní seznam je skupina úkolů. Můžete vytvořit tolik kontrolních seznamů, kolik potřebujete, a stejné úkoly můžete přiřadit více kontrolním seznamům. Při vytváření kontrolního seznamu určíte vlastníka a kalendář.

Pokud je pole **Typ úkolu** pro úkol je nastaveno na **Pozice**, **Manažer** nebo **Skupina**, ale z typu zadání nelze odvodit žádného konkrétního jedince, úkol bude přidělen vlastníkovi kontrolního seznamu. Zde je několik příkladů situací, kdy budou úkoly přiřazeny vlastníkovi kontrolního seznamu:

- Zaměstnanci, který je přijímán nebo propouštěn, není přiřazena žádná pozice. Protože zaměstnanec nemá přidělenou pozici, nelze určit jeho vedoucího.
- Pole **Typ úkolu** je nastaveno na **Pozice**, ale v době vytvoření úkolu není na pozici zařazen žádný zaměstnanec. Například úkol **Nastavení notebooku** je přiřazen k pozici číslo 000876 (**Specialista technické podpory**). V době, kdy je přijat zaměstnanec, není na pozici 000876 zařazen žádný zaměstnanec. Proto bude vytvořen úkol pro vlastníka kontrolního seznamu.
- Pole **Typ úkolu** je nastaveno na **Skupina**, ale v době vytvoření úkolu není na pozicích ve skupině zařazen žádný zaměstnanec.

Kalendář určený pro kontrolní seznam se používá k výpočtu termínu provedení úkolů, které jsou součástí tohoto kontrolního seznamu. Pracovní a nepracovní dny jsou definovány v nastavení kalendáře. Pracovní dny jsou zahrnuty, když se počítá splatnost úkolů, a dny pracovního klidu jsou vyloučeny. Mezi dny pracovního klidu patří víkendy a svátky. 

Po nastavení je kalendář spojen se šablonou kontrolního seznamu. Tímto způsobem se termín provedení každého úkolu v kontrolním seznamu vypočítá stejným způsobem. Můžete nastavit více kalendářů, ale ke každému kontrolnímu seznamu lze přiřadit pouze jeden kalendář.

## <a name="setting-up-assignment-groups-optional"></a>Nastavení skupin přiřazení (volitelné)

Někdy je za úkol zodpovědná skupina jednotlivců. Například skupina IT pracovníků může být zodpovědná za přípravu notebooků pro nové zaměstnance.

K nastavení skupiny přiřazení postupujte následovně.

1. Na stránce **Přiřazení skupiny** zvolte **Nový**.
1. Zadejte název (např. **IT notebook**) a popis skupiny.
1. Zvolte možnost **Uložit**.
1. Na záložce s náhledem **Členové** vyberte **Přidat**.
1. V poli **Pozice** vyberte všechny pozice, které jsou za úkol odpovědné.

Po vytvoření skupiny přiřazení je k dispozici pro výběr při vytvoření úkolu. Chcete-li pro úkol vybrat konkrétní skupinu, musíte vybrat **Skupina** v části **Typ přiřazení**. Skupina, kterou jste vytvořili, pak bude k dispozici pro výběr v poli **Přiřazený pro**.

> [!IMPORTANT]
> Pokud je úkol přiřazen skupině, je úkol označen jako **Dokončený**, když jej dokončí jeden člověk ve skupině. Úkoly se vytvářejí v době přijetí, propuštění nebo přechodu. Jsou vytvořeny pro uživatele, kteří jsou přiřazeni k pozicím, které jsou součástí skupiny.

## <a name="setting-up-task-groups-optional"></a>Nastavení skupin úkolů (volitelné)

Proces nasazení, rušení nebo přechodu může zahrnovat mnoho úkolů. Chcete-li usnadnit přiřazení všech požadovaných úkolů ke kontrolnímu seznamu, můžete vytvořit volitelné skupiny úkolů pro kategorizaci souvisejících úkolů. Například HR, IT a mzdová oddělení musí každé provést konkrétní úkoly, aby přijali nového zaměstnance. Proto vytvoříte následující skupiny úkolů: **HR**, **IT** a **Výplatní páska**. Když pak vytvoříte úkol, můžete k němu přiřadit jednu z těchto skupin úkolů.

Když chcete přidat úkol do kontrolního seznamu, můžete filtrovat seznam úkolů podle skupiny úkolů, ke které je požadovaný úkol přiřazen. Když například vytvoříte šablonu kontrolního seznamu, můžete seznam filtrovat tak, aby byly zobrazeny pouze úkoly IT, které jsou přiřazeny skupině úkolů **IT**. Můžete tedy zajistit, aby byly vybrány pouze relevantní IT úkoly.

## <a name="using-checklists"></a>Používání kontrolních seznamů

Když je pracovník přijat, propuštěn nebo převeden, lze vybrat jeden nebo více kontrolních seznamů. Termíny splnění úkolů a přiřazení pracovníků se vytvářejí po dokončení procesu přijetí, propuštění nebo přechodu. Například když vyberete tlačítko **Přijmout** nebo **Přijmout a zadat údaje**, jsou vytvořeny úkoly pro jednotlivce na základě typu přiřazení.

Ke každému úkolu je přiřazen termín splnění přičtením nebo odečtením posunu termínu splnění od data zahájení zaměstnance. Více informací naleznete v části [Termíny splnění úkolů a pole Posun termínu plnění](#task-due-dates-and-the-due-date-offset-field).

Pokud používáte personální akce, úkoly jsou vytvořeny, když je vybráno tlačítko **Dokončit** nebo je akce schválena.

V pracovním prostoru **Správa úkolů** můžete na zaměstnance použít kontrolní seznam tak, že zaměstnance vyberete na stránce jednoduchého seznamu nebo na stránce podrobností a poté vyberete **Použít kontrolní seznam**. Hodnota pole **Cílové datum** bude použita pro výpočet termínu provedení úkolů. Obvykle by cílové datum mělo odpovídat datu přijetí, propuštění nebo přechodu zaměstnance.

Kontrolní seznam můžete také použít na zaměstnance otevřením jeho stránky **Pracovník** a výběrem **Kontrolní seznamy** v nabídce.

## <a name="completing-tasks"></a>Provádění úkolů

Na stránce **Zaměstnanecká samoobsluha** může zaměstnanec zobrazit všechny úkoly, které jsou mu přiřazeny. Pro každý přidělený úkol jsou zobrazeny hodnoty **Úkol**, **Popis**, **Pokyny** a **Kontaktní osoba**. Kromě toho může zaměstnanec pro každý úkol otevřít přidruženou externí webovou stránku nebo přidruženou stránku v aplikaci Dynamics 365.

Úkoly lze také zobrazit na výchozím řídicím panelu. Chcete-li zobrazit úkoly na výchozím řídicím panelu:
1. Přejděte do části **Možnosti uživatele – Předvolby – Správa úloh** 
2. Nastavte možnost **Zobrazit úkoly na výchozím řídicím panelu** na **Zapnuto**.  

>[!Note] 
>Funkce **Správa úkolů** musí být ve **Správě funkcí** zapnutá, aby se možnost zobrazila v části **Uživatelské možnosti**.

Úkoly lze označit jako **Probíhající**, **Zrušené**, nebo **Dokončené**. Pokud byl úkol přiřazen skupině, bude označen jako **Dokončený**, když jej dokončí jeden člověk ve skupině.

Úkoly lze také znovu přiřadit.
