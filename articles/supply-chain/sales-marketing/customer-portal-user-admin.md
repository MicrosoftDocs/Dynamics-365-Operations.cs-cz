---
title: Vytváření a správa uživatelů zákaznického portálu
description: Toto téma vysvětluje, jak vytvořit uživatelské účty zákaznického portálu a nastavit pro ně oprávnění.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413943"
---
# <a name="create-and-manage-customer-portal-users"></a>Vytváření a správa uživatelů zákaznického portálu

V dodávané implementaci neexistuje žádný způsob, jak uživatele zaregistrovat pro weby vytvořené pomocí zákaznického portálu. Chcete-li se přihlásit a používat web, musí být uživatelé pozváni správcem. Microsoft úmyslně zablokoval možnost uživatelů se zaregistrovat.

Než může uživatel používat web, musí být pro něj vytvořen záznam kontaktu. Tento záznam uvádí, ke kterému zákaznickému účtu a právnické osobě uživatel patří. Tyto informace jsou nezbytné pro zajištění toho, aby uživatel mohl vytvářet a prohlížet prodejní objednávky.

Když se uživatelé zaregistrují, automaticky se pro ně vytvoří záznamy kontaktů. Proto nemůžete zajistit, aby si uživatel vybral správný zákaznický účet a právnickou osobu. Na druhé straně proces pozvání umožňuje správci přiřadit správný zákaznický účet a právnickou osobu k záznamu kontaktu před odesláním pozvání. Pokud přemýšlíte o přizpůsobení řešení, aby se uživatelé mohli zaregistrovat, nezapomeňte zvážit možné důsledky.

## <a name="prerequisite-setup"></a>Nastavení předpokladů

Kontakty v portálech Power Apps jsou uloženy jako záznamy v entitě **Kontakty** v Common Data Service. Dvojitý zápis pak tyto záznamy synchronizuje s Microsoft Dynamics 365 Supply Chain Management podle potřeby.

![![Systémový diagram pro kontakty zákaznického portálu](media/customer-portal-contacts.png "Systémový diagram pro kontakty zákaznického portálu")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Než začnete zvát nové zákazníky, ujistěte se, že jste povolili mapování entit **Kontakt** dvojitým zápisem.

## <a name="the-invitation-process"></a>Proces pozvání

Chcete-li pozvat stávající kontakt na zákaznický portál, postupujte podle kroků v [Pozvěte kontakty na své portály](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) v dokumentaci portálů Power Apps.

Než pozvete zákazníka, aby se připojil k zákaznickému portálu, ujistěte se, že [záznam kontaktu](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) zákazníka je k dispozici a nastaven následujícím způsobem:

1. Nastavte pole **Společnost** na právnickou osobu, do které má zázkazník patřit, v aplikaci Supply Chain Management.
2. Nastavte pole **Číslo účtu** na číslo účtu zákazníka, které má uživatel mít v aplikaci Supply Chain Management.

Po vytvoření kontaktu byste jej měli vidět v Supply Chain Management.

Další informace viz [Nakonfigurujte kontakt pro použití na portálu](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) v dokumentaci portálů Power Apps.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Dodávané webové role a oprávnění entit

Uživatelské role v portálech Power Apps jsou definovány [webovými rolemi](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) a [oprávněními entit](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). V zákaznickém portálu je definováno ihned několik rolí. Můžete vytvořit nové role a můžete upravit nebo odstranit stávající role.

### <a name="out-of-box-web-roles"></a>Dodávané webové role

Tato část popisuje webové role dodávané se zákaznickým portálem.

Další informace o tom, jak upravit dodávané uživatelské role, viz [Vytvářejte webové role pro portály](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) a [Přidejte zabezpečení založené na záznamu pomocí oprávnění entity pro portály](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) v dokumentaci portálů Power Apps.

#### <a name="administrator"></a>Správce

Správce dohlíží a udržuje web. Tato osoba zajistí a vytvoří zákaznický portál. Správce udržuje IT a bezpečnostní aspekty portálu a zajišťuje, aby vše probíhalo hladce. Správce může portál také přizpůsobit nebo změnit přidáním nových funkcí, vytvořením nových rolí a dalšími funkcemi.

#### <a name="customer-representative"></a>Zástupce zákazníka

Zástupce zákazníka pracuje pro zákaznickou společnost a odpovídá za správu objednávek, které společnost zadává. Zástupce zákazníka vidí všechny objednávky, které byly zadány pro společnost a uživatele, kteří je zadali. Zástupce zákazníka může navíc zobrazit informace o celkovém účtu a kontakty, které mohou zadávat objednávky jménem tohoto účtu.

#### <a name="authorized-users"></a>Oprávnění uživatelé

Oprávnění uživatelé mohou zadávat objednávky a zobrazovat stav objednávek, které zadali. Nemohou však zobrazit stav objednávek, které zadali jiní uživatelé v jejich společnosti.

#### <a name="unauthorized-users"></a>Neprávnění uživatelé

Neautorizovaní uživatelé nemohou zobrazit žádná data. Mohou vidět pouze veřejné informace, jako jsou smluvní podmínky a podrobnosti o společnosti, která provozuje zákaznický portál.

#### <a name="example"></a>Příklad

Následující tabulka ukazuje, které prodejní objednávky uživatelé v každé webové roli mohou v systému vidět.

| Prodejní objednávka | Správce | Zástupce zákazníka pro zákazníka&nbsp;X | Oprávněný uživatel: Jane | Oprávněný uživatel: Sam | Neprávněný uživatel: May |
|---|---|---|---|---|---|
| Zákazník&nbsp;X Objednatel:&nbsp;Jane | Ano | Ano | Ano | Žádný | Žádný |
| Zákazník&nbsp;X Objednatel:&nbsp;Sam | Ano | Ano | Žádný | Ano | Žádný |
| Zákazník&nbsp;Y Objednatel:&nbsp;May | Ano | Žádný | Žádný | Žádný | Žádný |

> [!NOTE]
> I když Sam a Jane jsou kontakty, které pracují pro zákazníka X, vidí pouze objednávky, které sami zadali, a nic jiného. Ačkoli May má v systému objednávku, nemůže ji vidět na zákaznickém portálu, protože je neoprávněným uživatelem. (Dále musí zadat objednávku prostřednictvím jiného kanálu, než je zákaznický portál.)
