---
title: Konfigurace typů pracovního volna a absence
description: Nastavte typy volna, které mohou zaměstnanci provést v aplikaci Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e35c5fed886ebf9a453c22b3e04ca9ffe50b6d70
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805197"
---
# <a name="configure-leave-and-absence-types"></a>Konfigurace typů pracovního volna a absence

[!include [preview banner](../includes/preview-banner.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Typy pracovního volna v Dynamics 365 Human Resources definují různé typy absence, které může zaměstnanec ohlásit. Typy pracovního volna můžete přizpůsobit podle potřeb dané organizace. Příklady popisů typů pracovního volna:

- Placený čas volna (PTO)
- Neplacené volno
- Placená dovolená
- Pracovní neschopnost
- Zdravotní dovolená
- Volno z rodinných důvodů
- Krátkodobá invalidita
- Volno z důvodu zármutku

## <a name="add-a-leave-type"></a>Přidání typu pracovního volna

1. V pracovním prostoru **Pracovní volno a absence** klikněte na kartu **Odkazy**.
2. V části **Nastavení** vyberte **Typ pracovního volna a absence**.
3. Zvolte **Nové**.
4. Zadejte název typu pracovního volna v části **Typ**, do pole **Popis** napište popis a vyberte pracovní postup v okně **ID pracovního postupu**. Na základě typu pracovního volna vyberte typ požadavku v poli **Typ požadavku**. Vyberte například **Volno** nebo **Dovolená**.
5. V části **Obecné** vyberte **Žádný**, **Naplánované** nebo **Neplánované** v rozevíracím seznamu **Kategorie**.
6. Vyberte kód výdělku z rozevíracího seznamu **kód výdělku**.
7. V části **Požadován kód důvodu** vyberte, zda chcete požadovat kód důvodu. Chcete-li požadovat kódy důvodu, budete je pravděpodobně muset přidat. V části **Kódy důvodu** vyberte možnost **Přidat**, vyberte kód důvodu a poté zaškrtněte políčko **Povoleno** vedle něho.
8. Je-li typ požadavku **Dovolená**, postupujte následovně:

      1. V části **S otevřeným koncem** vyberte, zda by uživatelé měli mít možnost vytvářet pracovní volna s otevřeným koncem.
      2. Pokud je možnost **S otevřeným koncem** aktivována, můžete vybrat, zda pracovníci musí po návratu z dovolené odeslat oznámení o návratu do práce.
      3. Pokud pracovníci musí odeslat oznámení o návratu do práce, můžete zapnout **Zapnout oznámení o návratu do práce**. Pokud je zapnuta možnost **Zapnout oznámení o návratu do práce** , položka **Vyžaduje se příloha** je automaticky aktivována a nelze ji deaktivovat.

9. Pokud by uživatelé měli nahrávat dokumenty při vytváření nebo aktualizaci žádostí o pracovní volno, můžete povolit **Vyžaduje se příloha**.
10. V části **Omezit přístup k vybraným rolím** vyberte, zda chcete omezit přístup. Poté vyberte role zabezpečení v části **Role zabezpečení pro tento typ pracovního volna**. Role zabezpečení jsou definovány v pracovním postupu vybraném pod položkou **ID pracovního postupu** dříve v tomto postupu.
11. Pod položkou **Barva kalendáře** zvolte barvu, která se má pro tento typ nepřítomnosti zobrazovat v kalendáři nepřítomností.
11. V možnosti **Vztahy přerušení** zvolte, zda chcete, aby tento typ dovolené buď pozastavil jiný typ dovolené, nebo aby byl pozastaven jiným typem dovolené. Pokud je pro typ přerušení volna podán požadavek na pracovní volno, automaticky se pro tento typ dovolené vytvoří přerušení volna.
12. Zvolte možnost **Uložit**.

## <a name="configure-leave-type-rules"></a>Konfigurace pravidel typů volna

1. Nastavte možnosti zaokrouhlení pro typ **Pracovní volno a absence**. Možnosti zahrnují **Žádný** **Nahoru**, **Dolů** a **Nejbližší**. Můžete také nastavit přesnost zaokrouhlení pro typ pracovního volna.
2. Nastavte **Oprava volna** pro typ pracovního volna. Pokud vyberete tuto možnost, počet svátků, které spadají do pracovního dne, bude použit k určení, jakým způsobem má být rozlišen volný čas u tohoto typu pracovního volna. Pokud například 1. svátek vánoční připadá na pondělí, odečte aplikace Human Resources při zpracování časového rozlišení od typu pracovního volna jeden den.

   Svátky nastavujete v kalendáři pracovní doby. Další informace naleznete v tématu [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md).
   
 3. Nastavte **Typ převodu pracovního volna** pro typ volna. Pokud vyberete tuto možnost, veškeré zůstatky k převodu budou převedeny na zadaný typ volna. Do plánu volna a nepřítomnosti musí být rovněž zahrnut typ převodu volna. 
 
4. Definujte **Pravidla vypršení platnosti** pro typ volna. Když nakonfigurujete tuto možnost, můžete vybrat jednotku dní nebo měsíců a nastavit dobu trvání. Datum účinnosti oravidla ukončení platnosti se používá k určení, kdy se má spustit dávková úloha, která zpracovává vypršení platnosti volna, nebo datum, kdy se pravidlo projeví. Samotné vypršení platnosti nastane vždy k datu zahájení období časového rozlišení. Například pokud je datem zahájení období časového rozlišení 3. srpna 2021 a pravidlo vypršení platnosti bylo nastaveno na 6 měsíců, bude pravidlo zpracováno na základě offsetu vypršení platnosti od data zahájení období časového rozlišení, takže by bylo provedeno 3. února 2022. Jakékoli zůstatky dovolené, které existují v době vypršení platnosti, budou odečteny od typu dovolené a budou zohledněny v zůstatku dovolené.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Nakonfigurujte požadovanou přílohu podle typu dovolené

> [!NOTE]
> Chcete-li použít pole **Je vyžadována příloha**, musíte nejprve zapnout funkci **Nakonfigurujte požadovanou přílohu pro žádosti o dovolenou** ve Správě funkcí. Další informace o zapnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

1. Na stránce **Dovolená a nepřítomnost** na kartě **Odkazy** v **Nastavení** vyberte **Typy dovolené a nepřítomnosti**.

2. V seznamu vyberte **Typ dovolené a nepřítomnosti**. V sekci **Všeobecné** použijte pole **Je vyžadována příloha** pro určení, zda musí být příloha nahrána, když zaměstnanec odešle nový požadavek na dovolenou pro vybraný typ dovolené. 

Zaměstnanci budou povinni nahrát přílohu, když předloží novou žádost o dovolenou, která má typ dovolené, kde je povoleno pole **Je vyžadována příloha**. Chcete-li zobrazit přílohu, která byla nahrána jako součást žádosti o dovolenou, mohou schvalovatelé žádosti o dovolenou použít možnost **Přílohy** pro pracovní položky, které jsou jim přiřazeny. Pokud k žádosti o dovolenou přistupujete pomocí aplikace Human Resources v Microsoft Teams, možnost **Zobrazit podrobnosti** pro žádost o dovolenou lze použít k zobrazení jejích podrobností a všech příloh.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Nakonfigurovat jednotky dovolené (hodiny/dny) podle typu pracovního volna

> [!NOTE]
> Chcete-li použít funkci jednotek dovolené na typ dovolené, musíte nejprve zapnout funkci **Nakonfigurujte jednotky dovolené pro každý typ dovolené** ve Správě funkcí. Další informace o zapnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

> [!IMPORTANT]
> Ve výchozím nastavení typy dovolené v právnické osobě používají jednotky dovolené z konfigurace parametrů dovolené na úrovni právnické osoby.
> 
> Jednotku dovolené typu dovolené a nepřítomnosti lze upravit pouze v případě, že pro daný typ dovolené neexistují žádné dovolené.
> 
> Poté, co funkci zapnete, ji nelze vypnout.

1. Na stránce **Dovolená a nepřítomnost** na kartě **Odkazy** v **Nastavení** vyberte **Typy dovolené a nepřítomnosti**.

2. V seznamu vyberte typ dovolené a nepřítomnosti. Pak v sekci **Všeobecné** v poli **Jednotka** vyberte jednotku dovolené. Můžete vybrat **Hodiny** nebo **Dny**.

3. Volitelné: Pokud jste vybrali **Hodiny** v poli **Jednotka**, můžete použít pole **Povolit půldenní definici** a určete, zda si zaměstnanci mohou vybrat první půlden nebo druhý půlden volna, pokud žádají o půldenní volno.

Zaměstnanci, kteří podají novou žádost o dovolenou, si mohou pro sestavení žádosti o dovolenou vybrat různé typy dovolené. Všechny typy dovolené, které jsou vybrány jako součást jednoho požadavku na dovolenou, by však měly mít stejnou jednotku dovolené. Zaměstnanci mohou zobrazit jednotku dovolené pro každý typ dovolené ve formuláři **Žádost o volno**.

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Vytvoření plánu pracovního volna a absence](hr-leave-and-absence-plans.md)
- [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md)
- [Přerušit pracovní volno](hr-leave-and-absence-suspend-leave.md)
- [Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
