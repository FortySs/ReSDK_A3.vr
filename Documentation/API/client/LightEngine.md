# LightEngine.h

## lightObject

Type: constant

Description: #define usedebuglightrender


Replaced value:
```sqf
_light
```
File: [client\LightEngine\LightEngine.h at line 9](../../../Src/client/LightEngine/LightEngine.h#L9)
## sourceObject

Type: constant

Description: 


Replaced value:
```sqf
_source
```
File: [client\LightEngine\LightEngine.h at line 11](../../../Src/client/LightEngine/LightEngine.h#L11)
## allEmitters

Type: constant

Description: 


Replaced value:
```sqf
_allEmitters
```
File: [client\LightEngine\LightEngine.h at line 13](../../../Src/client/LightEngine/LightEngine.h#L13)
## le_light_max_index

Type: constant

Description: 


Replaced value:
```sqf
1999
```
File: [client\LightEngine\LightEngine.h at line 15](../../../Src/client/LightEngine/LightEngine.h#L15)
## emitterObject

Type: constant

Description: 


Replaced value:
```sqf
_effEmitter
```
File: [client\LightEngine\LightEngine.h at line 17](../../../Src/client/LightEngine/LightEngine.h#L17)
## regVST(type)

Type: constant

Description: visual states functionality
- Param: type

Replaced value:
```sqf
le_conf_##type = { params ["_condit","_src",["_ctxParams",0]]; private __GLOB_CFG_IDX__ = type ;
```
File: [client\LightEngine\LightEngine.h at line 20](../../../Src/client/LightEngine/LightEngine.h#L20)
## vstParams

Type: constant

Description: 


Replaced value:
```sqf
_ctxParams
```
File: [client\LightEngine\LightEngine.h at line 21](../../../Src/client/LightEngine/LightEngine.h#L21)
## src

Type: constant

Description: source object who inited vst


Replaced value:
```sqf
_src
```
File: [client\LightEngine\LightEngine.h at line 23](../../../Src/client/LightEngine/LightEngine.h#L23)
## localPlayer

Type: constant

Description: local player == this


Replaced value:
```sqf
__LOCAL_PLAYER__
```
File: [client\LightEngine\LightEngine.h at line 26](../../../Src/client/LightEngine/LightEngine.h#L26)
## VST_COND_CREATE

Type: constant

Description: 


Replaced value:
```sqf
1
```
File: [client\LightEngine\LightEngine.h at line 27](../../../Src/client/LightEngine/LightEngine.h#L27)
## VST_COND_DESTR

Type: constant

Description: 


Replaced value:
```sqf
0
```
File: [client\LightEngine\LightEngine.h at line 28](../../../Src/client/LightEngine/LightEngine.h#L28)
## vstIsState(state)

Type: constant

Description: 
- Param: state

Replaced value:
```sqf
(state == _condit)
```
File: [client\LightEngine\LightEngine.h at line 29](../../../Src/client/LightEngine/LightEngine.h#L29)
## VSTCreate

Type: constant

Description: 


Replaced value:
```sqf
if (_condit == VST_COND_CREATE) exitWith
```
File: [client\LightEngine\LightEngine.h at line 30](../../../Src/client/LightEngine/LightEngine.h#L30)
## VSTDestroy

Type: constant

Description: 


Replaced value:
```sqf
if (_condit == VST_COND_DESTR) exitWith
```
File: [client\LightEngine\LightEngine.h at line 31](../../../Src/client/LightEngine/LightEngine.h#L31)
## endRegVST

Type: constant

Description: 


Replaced value:
```sqf
};
```
File: [client\LightEngine\LightEngine.h at line 33](../../../Src/client/LightEngine/LightEngine.h#L33)
## update_delay_mainThread

Type: constant

Description: !not used


Replaced value:
```sqf
0.01
```
File: [client\LightEngine\LightEngine.h at line 37](../../../Src/client/LightEngine/LightEngine.h#L37)
## le_firelight_startindex

Type: constant

Description: начальное число индексатора для firelight событий (исключая его)


Replaced value:
```sqf
5000
```
File: [client\LightEngine\LightEngine.h at line 40](../../../Src/client/LightEngine/LightEngine.h#L40)
## le_shot_startindex

Type: constant

Description: начальное число индексатора для shot событий (исключая его)


Replaced value:
```sqf
10000
```
File: [client\LightEngine\LightEngine.h at line 62](../../../Src/client/LightEngine/LightEngine.h#L62)
## shotParams

Type: constant

Description: 


Replaced value:
```sqf
_shotParams
```
File: [client\LightEngine\LightEngine.h at line 64](../../../Src/client/LightEngine/LightEngine.h#L64)
## regShot(type)

Type: constant

Description: 
- Param: type

Replaced value:
```sqf
_rshot_t = type; _rfl_ev = {params ['sourceObject','shotParams']; private __disposable = [];
```
File: [client\LightEngine\LightEngine.h at line 66](../../../Src/client/LightEngine/LightEngine.h#L66)
## makeParticle(namevar)

Type: constant

Description: 
- Param: namevar

Replaced value:
```sqf
namevar = "#particlesource" createVehicleLocal [0,0,0]; __disposable pushBack namevar
```
File: [client\LightEngine\LightEngine.h at line 67](../../../Src/client/LightEngine/LightEngine.h#L67)
## makeLight(namevar)

Type: constant

Description: 
- Param: namevar

Replaced value:
```sqf
namevar = "#lightpoint" createVehicleLocal [0,0,0]; __disposable pushBack namevar
```
File: [client\LightEngine\LightEngine.h at line 68](../../../Src/client/LightEngine/LightEngine.h#L68)
## disposeAllAfterTime(time)

Type: constant

Description: 
- Param: time

Replaced value:
```sqf
invokeAfterDelayParams({{deleteVehicle _x}count _this},time,__disposable)
```
File: [client\LightEngine\LightEngine.h at line 70](../../../Src/client/LightEngine/LightEngine.h#L70)
## linkObject(light,object,anotherParams)

Type: constant

Description: 
- Param: light
- Param: object
- Param: anotherParams

Replaced value:
```sqf
light attachto [object,anotherParams]
```
File: [client\LightEngine\LightEngine.h at line 72](../../../Src/client/LightEngine/LightEngine.h#L72)
## endRegShot

Type: constant

Description: 


Replaced value:
```sqf
}; missionNamespace setVariable ["le_conf_shot_" + str(_rshot_t - le_shot_startindex),_rfl_ev];
```
File: [client\LightEngine\LightEngine.h at line 74](../../../Src/client/LightEngine/LightEngine.h#L74)
## SCRIPT_EMIT_HANDLER_MODE_DEFAULT

Type: constant

Description: стандартный обработчик скриптовых эффектов


Replaced value:
```sqf
0
```
File: [client\LightEngine\LightEngine.h at line 84](../../../Src/client/LightEngine/LightEngine.h#L84)
## SCRIPT_EMIT_HANDLER_MODE_DROP

Type: constant

Description: скриптовый обработчик дроппер. основная особенность - не создает направленные источники, удаляется самостоятельно


Replaced value:
```sqf
1
```
File: [client\LightEngine\LightEngine.h at line 86](../../../Src/client/LightEngine/LightEngine.h#L86)
## SCRIPT_EMIT_HANDLER_MODE_UNMANAGED

Type: constant

Description: скриптовый обработчик неуправляемый. основная особенность - не привязан к объекту, создается в позиции. пользователь самостоятельно должен удалять его


Replaced value:
```sqf
2
```
File: [client\LightEngine\LightEngine.h at line 88](../../../Src/client/LightEngine/LightEngine.h#L88)
## regScriptEmit(type)

Type: constant

Description: scripted emitters
- Param: type

Replaced value:
```sqf
_semDat = []; le_se_map set ['type',_semDat]; le_conf_##type = { \
	params ['sourceObject']; \
	sourceObject setvariable ["__config",type]; \
	private allEmitters = []; \
	sourceObject setVariable ["__allEmitters",allEmitters]; \
	[(le_se_map get 'type')] call le_se_handleConfig; \
};	_semDat append [
```
File: [client\LightEngine\LightEngine.h at line 93](../../../Src/client/LightEngine/LightEngine.h#L93)
## endScriptEmit

Type: constant

Description: 


Replaced value:
```sqf
] ;
```
File: [client\LightEngine\LightEngine.h at line 101](../../../Src/client/LightEngine/LightEngine.h#L101)
## _emitAlias(strval)

Type: constant

Description: уникальный алиас
- Param: strval

Replaced value:
```sqf
["alias",strval],
```
File: [client\LightEngine\LightEngine.h at line 104](../../../Src/client/LightEngine/LightEngine.h#L104)
## type

Type: function

Description: 
- Param: _condit
- Param: _src
- Param: _ctxParams (optional, default 0)

File: [client\LightEngine\LightEngine.h at line 93](../../../Src/client/LightEngine/LightEngine.h#L93)
# LightEngine.hpp

## SHOT_MEATSPLAT

Type: constant

Description: shotable effects start only after 10000 (le_shot_startindex)


Replaced value:
```sqf
10001
```
File: [client\LightEngine\LightEngine.hpp at line 7](../../../Src/client/LightEngine/LightEngine.hpp#L7)
## SHOT_DESTROYLIMB

Type: constant

Description: 


Replaced value:
```sqf
10002
```
File: [client\LightEngine\LightEngine.hpp at line 8](../../../Src/client/LightEngine/LightEngine.hpp#L8)
## SHOT_BULLET_PISTOL

Type: constant

Description: 


Replaced value:
```sqf
10003
```
File: [client\LightEngine\LightEngine.hpp at line 9](../../../Src/client/LightEngine/LightEngine.hpp#L9)
## SHOT_BULLET_SHOTGUN

Type: constant

Description: 


Replaced value:
```sqf
10004
```
File: [client\LightEngine\LightEngine.hpp at line 10](../../../Src/client/LightEngine/LightEngine.hpp#L10)
## SHOT_BULLET_SHOTRIFLE

Type: constant

Description: 


Replaced value:
```sqf
10005
```
File: [client\LightEngine\LightEngine.hpp at line 11](../../../Src/client/LightEngine/LightEngine.hpp#L11)
## VST_EATER_NIGHTVISION

Type: constant

Description: visual states start only after 20000


Replaced value:
```sqf
20001
```
File: [client\LightEngine\LightEngine.hpp at line 14](../../../Src/client/LightEngine/LightEngine.hpp#L14)
## VST_HUMAN_STEALTH

Type: constant

Description: 


Replaced value:
```sqf
20002
```
File: [client\LightEngine\LightEngine.hpp at line 15](../../../Src/client/LightEngine/LightEngine.hpp#L15)
## VST_CLOTH_BREASTPLATE

Type: constant

Description: 


Replaced value:
```sqf
20003
```
File: [client\LightEngine\LightEngine.hpp at line 16](../../../Src/client/LightEngine/LightEngine.hpp#L16)
## VST_CLOTH_CERAMIC

Type: constant

Description: 


Replaced value:
```sqf
20004
```
File: [client\LightEngine\LightEngine.hpp at line 17](../../../Src/client/LightEngine/LightEngine.hpp#L17)
## VST_CLOTH_STRONGARMOR

Type: constant

Description: 


Replaced value:
```sqf
20005
```
File: [client\LightEngine\LightEngine.hpp at line 18](../../../Src/client/LightEngine/LightEngine.hpp#L18)
## VST_CLOTH_METALARMOR

Type: constant

Description: 


Replaced value:
```sqf
20006
```
File: [client\LightEngine\LightEngine.hpp at line 19](../../../Src/client/LightEngine/LightEngine.hpp#L19)
## VST_CLOTH_FLEXIBLEARMOR

Type: constant

Description: 


Replaced value:
```sqf
20007
```
File: [client\LightEngine\LightEngine.hpp at line 20](../../../Src/client/LightEngine/LightEngine.hpp#L20)
## VST_GHOST_EFFECT

Type: constant

Description: 


Replaced value:
```sqf
20008
```
File: [client\LightEngine\LightEngine.hpp at line 21](../../../Src/client/LightEngine/LightEngine.hpp#L21)
## VST_ATTACHED_OBJECTS

Type: constant

Description: 


Replaced value:
```sqf
20009
```
File: [client\LightEngine\LightEngine.hpp at line 22](../../../Src/client/LightEngine/LightEngine.hpp#L22)
# LightEngine.sqf

## le_simulated

Type: Variable

Description: Нужно выяснить какое существо самое лучшее в плане атачинга при первом создании


Initial value:
```sqf
clientMob//"B_Soldier_F" createVehicleLocal [0,0,0]
```
File: [client\LightEngine\LightEngine.sqf at line 41](../../../Src/client/LightEngine/LightEngine.sqf#L41)
## le_allChunkTypes

Type: Variable

Description: le_localGlsData = nullPtr;


Initial value:
```sqf
[CHUNK_TYPE_ITEM,CHUNK_TYPE_STRUCTURE,CHUNK_TYPE_DECOR]
```
File: [client\LightEngine\LightEngine.sqf at line 48](../../../Src/client/LightEngine/LightEngine.sqf#L48)
## le_allLights

Type: Variable

Description: 


Initial value:
```sqf
[] //all light points
```
File: [client\LightEngine\LightEngine.sqf at line 50](../../../Src/client/LightEngine/LightEngine.sqf#L50)
## le_initializeScriptedConfigs

Type: function

Description: prepare cfgs, called on serverside


File: [client\LightEngine\LightEngine.sqf at line 18](../../../Src/client/LightEngine/LightEngine.sqf#L18)
## le_loadLight

Type: function

Description: загружает источник освещения или частиц
- Param: _type (optional, default -1)
- Param: _src

File: [client\LightEngine\LightEngine.sqf at line 72](../../../Src/client/LightEngine/LightEngine.sqf#L72)
## le_doShot

Type: function

Description: };
- Param: _type
- Param: _src
- Param: _ctxParams (optional, default [])

File: [client\LightEngine\LightEngine.sqf at line 126](../../../Src/client/LightEngine/LightEngine.sqf#L126)
## le_unloadLight

Type: function

Description: выгружает источник освещения
- Param: _obj

File: [client\LightEngine\LightEngine.sqf at line 143](../../../Src/client/LightEngine/LightEngine.sqf#L143)
## le_isLoadedLight

Type: function

Description: проверяет висит ли на объекте источник света
- Param: _obj

File: [client\LightEngine\LightEngine.sqf at line 172](../../../Src/client/LightEngine/LightEngine.sqf#L172)
## le_getLoadedLightCfg

Type: function

Description: 
- Param: _obj

File: [client\LightEngine\LightEngine.sqf at line 178](../../../Src/client/LightEngine/LightEngine.sqf#L178)
## le_isLightConfig

Type: function

Description: 


File: [client\LightEngine\LightEngine.sqf at line 185](../../../Src/client/LightEngine/LightEngine.sqf#L185)
## le_isShotConfig

Type: function

Description: 


File: [client\LightEngine\LightEngine.sqf at line 189](../../../Src/client/LightEngine/LightEngine.sqf#L189)
## le_debug_canViewLight

Type: function

Description: 
- Param: _src
- Param: _isLightObject

File: [client\LightEngine\LightEngine.sqf at line 227](../../../Src/client/LightEngine/LightEngine.sqf#L227)
# LightEngine_mainThread.sqf

## loadLightOnObject(_x)

Type: constant

Description: 
- Param: _x

Replaced value:
```sqf
[_x getVariable "light",_x] call le_loadLight
```
File: [client\LightEngine\LightEngine_mainThread.sqf at line 48](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L48)
## unloadLightOnObject(_x)

Type: constant

Description: 
- Param: _x

Replaced value:
```sqf
[_x] call le_unloadLight
```
File: [client\LightEngine\LightEngine_mainThread.sqf at line 49](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L49)
## __chunkToGLSType()

Type: constant

Description: 
- Param: 

Replaced value:
```sqf
(format["%1:%2:%3",_type,_cx,_cy])
```
File: [client\LightEngine\LightEngine_mainThread.sqf at line 51](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L51)
## __compareHashesStr()

Type: constant

Description: 
- Param: 

Replaced value:
```sqf
(format["G:%1 -> L:%2",_hash,_localHash])
```
File: [client\LightEngine\LightEngine_mainThread.sqf at line 52](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L52)
## le_lastChunkItem

Type: Variable

Description: ! This file not used.


Initial value:
```sqf
null
```
File: [client\LightEngine\LightEngine_mainThread.sqf at line 8](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L8)
## le_lastChunkStructure

Type: Variable

Description: 


Initial value:
```sqf
null
```
File: [client\LightEngine\LightEngine_mainThread.sqf at line 9](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L9)
## le_onUpdate

Type: function

Description: основной поток обновления


File: [client\LightEngine\LightEngine_mainThread.sqf at line 12](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L12)
## le_collectAroundChunks

Type: function

Description: 
- Param: _loadList
- Param: _chunk
- Param: _chunkType

File: [client\LightEngine\LightEngine_mainThread.sqf at line 111](../../../Src/client/LightEngine/LightEngine_mainThread.sqf#L111)
# LightEngine_ScriptedCulling.sqf

## LESC_USE_FAST_UPDATE

Type: constant

Description: #define LESC_ENABLE_CULLING


Replaced value:
```sqf

```
File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 15](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L15)
## lesc_list_allObjects

Type: Variable

Description: 


Initial value:
```sqf
[]
```
File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 269](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L269)
## lesc_list_allDataObjs

Type: Variable

Description: 


Initial value:
```sqf
[]
```
File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 273](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L273)
## lesc_cullCnt

Type: Variable

Description: 


Initial value:
```sqf
0
```
File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 350](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L350)
## lesc_setDebugRender

Type: function

> Exists if **EDITOR** defined

Description: 
- Param: _mode

File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 261](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L261)
## lesc_handleLight

Type: function

Description: 
- Param: _lt
- Param: _isDirect (optional, default false)

File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 280](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L280)
## lesc_onLightRemove

Type: function

Description: 
- Param: _dummyParam

File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 300](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L300)
## lesc_handleProp

Type: function

Description: 
- Param: _o
- Param: _prop
- Param: _val

File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 314](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L314)
## lesc_cullingProcess

Type: function

Description: 


File: [client\LightEngine\LightEngine_ScriptedCulling.sqf at line 353](../../../Src/client/LightEngine/LightEngine_ScriptedCulling.sqf#L353)
# LightRender.sqf

## LIGHT_RENDER_PRINT_ERROR_IF_NOT_INIT_ON_CUSTOM

Type: constant

Description: todo doc update


Replaced value:
```sqf

```
File: [client\LightEngine\LightRender.sqf at line 9](../../../Src/client/LightEngine/LightRender.sqf#L9)
## NEW_ALGORITHM_LIGHT_RENDERING

Type: constant

Description: Новый алгоритм затухания и появления света. С первой легаси версии является основным способом рендеринга света


Replaced value:
```sqf

```
File: [client\LightEngine\LightRender.sqf at line 12](../../../Src/client/LightEngine/LightRender.sqf#L12)
## BRIGHT_CHANGE_VALUE_ON_FRAME

Type: constant

Description: как я понял расчёт по кадрам


Replaced value:
```sqf
10
```
File: [client\LightEngine\LightRender.sqf at line 15](../../../Src/client/LightEngine/LightRender.sqf#L15)
## LE_RENDER_DISTANCE_ONCHECK

Type: constant

Description: дистанция отрисовки света если локальный игрок не смотрит на него


Replaced value:
```sqf
7
```
File: [client\LightEngine\LightRender.sqf at line 20](../../../Src/client/LightEngine/LightRender.sqf#L20)
## distRad

Type: constant

Description: 


Replaced value:
```sqf
1400.5
```
File: [client\LightEngine\LightRender.sqf at line 49](../../../Src/client/LightEngine/LightRender.sqf#L49)
## upperMax

Type: constant

Description: 


Replaced value:
```sqf
1000
```
File: [client\LightEngine\LightRender.sqf at line 50](../../../Src/client/LightEngine/LightRender.sqf#L50)
## constbias

Type: constant

Description: lastpos_cached = _npos;


Replaced value:
```sqf
0.1
```
File: [client\LightEngine\LightRender.sqf at line 151](../../../Src/client/LightEngine/LightRender.sqf#L151)
## gvar(obj,val)

Type: constant

Description: _eyeZ = eyepos player select 2;
- Param: obj
- Param: val

Replaced value:
```sqf
(obj getvariable #val)
```
File: [client\LightEngine\LightRender.sqf at line 160](../../../Src/client/LightEngine/LightRender.sqf#L160)
## gvardef(obj,val,def)

Type: constant

Description: 
- Param: obj
- Param: val
- Param: def

Replaced value:
```sqf
(obj getvariable [#val,def])
```
File: [client\LightEngine\LightRender.sqf at line 161](../../../Src/client/LightEngine/LightRender.sqf#L161)
## svar(obj,var,val)

Type: constant

Description: 
- Param: obj
- Param: var
- Param: val

Replaced value:
```sqf
obj setvariable [#var,val]
```
File: [client\LightEngine\LightRender.sqf at line 162](../../../Src/client/LightEngine/LightRender.sqf#L162)
## timetofadelight

Type: constant

Description: 


Replaced value:
```sqf
0.05
```
File: [client\LightEngine\LightRender.sqf at line 163](../../../Src/client/LightEngine/LightRender.sqf#L163)
## le_list_changevis

Type: Variable

Description: structs in type: src,lt,curview,


Initial value:
```sqf
[]
```
File: [client\LightEngine\LightRender.sqf at line 29](../../../Src/client/LightEngine/LightRender.sqf#L29)
## le_render_handleState

Type: Variable

> Exists if **NEW_ALGORITHM_LIGHT_RENDERING** defined

Description: 


Initial value:
```sqf
startUpdate(le_onchangeview,0)
```
File: [client\LightEngine\LightRender.sqf at line 307](../../../Src/client/LightEngine/LightRender.sqf#L307)
## le_render_handleUpdate

Type: Variable

Description: 


Initial value:
```sqf
startUpdate(le_onupdrender,0)
```
File: [client\LightEngine\LightRender.sqf at line 310](../../../Src/client/LightEngine/LightRender.sqf#L310)
## le_initRenderer

Type: function

Description: 
- Param: _obj

File: [client\LightEngine\LightRender.sqf at line 31](../../../Src/client/LightEngine/LightRender.sqf#L31)
## le_render_findUpSide

Type: function

Description: 


File: [client\LightEngine\LightRender.sqf at line 46](../../../Src/client/LightEngine/LightRender.sqf#L46)
## le_addTransitionState

Type: function

Description: if _mode then do render else hide
- Param: _src
- Param: _mode

File: [client\LightEngine\LightRender.sqf at line 79](../../../Src/client/LightEngine/LightRender.sqf#L79)
## le_onupdrender

Type: function

Description: 


File: [client\LightEngine\LightRender.sqf at line 106](../../../Src/client/LightEngine/LightRender.sqf#L106)
## le_onchangeview

Type: function

Description: 
- Param: _src
- Param: _lt
- Param: _curval
- Param: _modif
- Param: _mode

File: [client\LightEngine\LightRender.sqf at line 259](../../../Src/client/LightEngine/LightRender.sqf#L259)
# ScriptedEffects.sqf

## le_se_map

Type: Variable

Description: карта эффектов. ключи - айди эффектов, значения - настройки эмиттеров


Initial value:
```sqf
createHashMap
```
File: [client\LightEngine\ScriptedEffects.sqf at line 11](../../../Src/client/LightEngine/ScriptedEffects.sqf#L11)
## le_se_noattr

Type: Variable

Description: 


Initial value:
```sqf
null //!not used
```
File: [client\LightEngine\ScriptedEffects.sqf at line 12](../../../Src/client/LightEngine/ScriptedEffects.sqf#L12)
## le_se_cfgRange

Type: Variable

Description: !not used


Initial value:
```sqf
[2100,4900]
```
File: [client\LightEngine\ScriptedEffects.sqf at line 13](../../../Src/client/LightEngine/ScriptedEffects.sqf#L13)
## le_se_map_cfgHandlers

Type: Variable

Description: 


Initial value:
```sqf
createHashMap //карта зарегистрированных конфигов
```
File: [client\LightEngine\ScriptedEffects.sqf at line 206](../../../Src/client/LightEngine/ScriptedEffects.sqf#L206)
## le_se_mapHandlersUnmanaged

Type: Variable

Description: 


Initial value:
```sqf
null //карта нативных эффектов
```
File: [client\LightEngine\ScriptedEffects.sqf at line 211](../../../Src/client/LightEngine/ScriptedEffects.sqf#L211)
## le_se_mapHandlersShots

Type: Variable

Description: карта нативных эффектов


Initial value:
```sqf
null
```
File: [client\LightEngine\ScriptedEffects.sqf at line 212](../../../Src/client/LightEngine/ScriptedEffects.sqf#L212)
## le_se_mapHandlers

Type: Variable

Description: 


Initial value:
```sqf
createHashMapFromArray [...
```
File: [client\LightEngine\ScriptedEffects.sqf at line 219](../../../Src/client/LightEngine/ScriptedEffects.sqf#L219)
## le_se_map_partAddress

Type: Variable

Description: 


Initial value:
```sqf
createHashMap //key setParticleN , value [functions]
```
File: [client\LightEngine\ScriptedEffects.sqf at line 476](../../../Src/client/LightEngine/ScriptedEffects.sqf#L476)
## le_se_list_fassoc

Type: Variable

Description: see macro SCRIPT_EMIT_HANDLER_MODE_


Initial value:
```sqf
[]
```
File: [client\LightEngine\ScriptedEffects.sqf at line 579](../../../Src/client/LightEngine/ScriptedEffects.sqf#L579)
## le_se_handleConfig

Type: function

Description: Функция-обработчик скриптового освещения (для клиента)
- Param: _cfgDataList
- Param: _hMode (optional, default SCRIPT_EMIT_HANDLER_MODE_DEFAULT)
- Param: _dropPos

File: [client\LightEngine\ScriptedEffects.sqf at line 36](../../../Src/client/LightEngine/ScriptedEffects.sqf#L36)
## le_se_createUnmanagedEmitter

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 138](../../../Src/client/LightEngine/ScriptedEffects.sqf#L138)
## le_se_handleCfgEvents

Type: function

Description: 
- Param: _cfgName
- Param: _cfgInParams

File: [client\LightEngine\ScriptedEffects.sqf at line 159](../../../Src/client/LightEngine/ScriptedEffects.sqf#L159)
## le_se_internal_errorFuncCfgEvents

Type: function

Description: 
- Param: _errpar

File: [client\LightEngine\ScriptedEffects.sqf at line 173](../../../Src/client/LightEngine/ScriptedEffects.sqf#L173)
## le_se_registerConfigHandler

Type: function

Description: 
- Param: _cfgName
- Param: _cfgCode

File: [client\LightEngine\ScriptedEffects.sqf at line 177](../../../Src/client/LightEngine/ScriptedEffects.sqf#L177)
## le_se_isAttachedToMob

Type: function

Description: работает внутри обработчика скрипта для эмиттера. проверяет является ли контекст подключением к мобу


File: [client\LightEngine\ScriptedEffects.sqf at line 183](../../../Src/client/LightEngine/ScriptedEffects.sqf#L183)
## le_se_getAttachedProxySlot

Type: function

Description: получает айди слота подключения к мобу (например INV_FACE)


File: [client\LightEngine\ScriptedEffects.sqf at line 188](../../../Src/client/LightEngine/ScriptedEffects.sqf#L188)
## le_se_getCurrentConfigPropVal

Type: function

Description: получает значение опции из конфига. используется в хандлерах событий скриптовых эмиттеров
- Param: _srch

File: [client\LightEngine\ScriptedEffects.sqf at line 193](../../../Src/client/LightEngine/ScriptedEffects.sqf#L193)
## le_se_getCurrentConfigId

Type: function

Description: получает айди текущего конфига. только внутри хандлееров событий скриптовых эмиттеров


File: [client\LightEngine\ScriptedEffects.sqf at line 202](../../../Src/client/LightEngine/ScriptedEffects.sqf#L202)
## le_se_getSimProxObj

Type: function

Description: специальная функция разрешения симуляции для игры и для редактора


File: [client\LightEngine\ScriptedEffects.sqf at line 215](../../../Src/client/LightEngine/ScriptedEffects.sqf#L215)
## le_se_errorHandler

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 255](../../../Src/client/LightEngine/ScriptedEffects.sqf#L255)
## le_se_intenral_handleVarInit

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 259](../../../Src/client/LightEngine/ScriptedEffects.sqf#L259)
## le_se_internal_createDropEmitterMap

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 273](../../../Src/client/LightEngine/ScriptedEffects.sqf#L273)
## le_se_internal_createUnmanagedEmitterMap

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 321](../../../Src/client/LightEngine/ScriptedEffects.sqf#L321)
## le_se_intenral_handleUnmanagedVarInit

Type: function

Description: 
- Param: _prop
- Param: _val

File: [client\LightEngine\ScriptedEffects.sqf at line 340](../../../Src/client/LightEngine/ScriptedEffects.sqf#L340)
## le_se_intenral_handleDropVarInit

Type: function

Description: 
- Param: _prop
- Param: _val

File: [client\LightEngine\ScriptedEffects.sqf at line 357](../../../Src/client/LightEngine/ScriptedEffects.sqf#L357)
## le_se_fireEmit

Type: function

Description: 
- Param: _cfg
- Param: _pos
- Param: _norm (optional, default ['0', '0', '1'])
- Param: _deleteAfter
- Param: _refemitters
- Param: _reservedParam

File: [client\LightEngine\ScriptedEffects.sqf at line 365](../../../Src/client/LightEngine/ScriptedEffects.sqf#L365)
## le_se_initScriptedLights

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 406](../../../Src/client/LightEngine/ScriptedEffects.sqf#L406)
## le_se_doSorting

Type: function

Description: Спасибо Богемия...


File: [client\LightEngine\ScriptedEffects.sqf at line 429](../../../Src/client/LightEngine/ScriptedEffects.sqf#L429)
## le_se_getParticleOption

Type: function

Description: key setParticleN , value [functions]
- Param: _optName
- Param: _varname
- Param: _storage

File: [client\LightEngine\ScriptedEffects.sqf at line 477](../../../Src/client/LightEngine/ScriptedEffects.sqf#L477)
## le_se_setParticleOption

Type: function

Description: 
- Param: _optName
- Param: _varname
- Param: _storage
- Param: _value

File: [client\LightEngine\ScriptedEffects.sqf at line 486](../../../Src/client/LightEngine/ScriptedEffects.sqf#L486)
## le_se_getCurrentEmitterIndex

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 495](../../../Src/client/LightEngine/ScriptedEffects.sqf#L495)
## le_se_internal_generateOptionAddress

Type: function

Description: 


File: [client\LightEngine\ScriptedEffects.sqf at line 497](../../../Src/client/LightEngine/ScriptedEffects.sqf#L497)
# VisualStatesConfigs.sqf

## VAR_FULL_PREFIX__VST_PRIVATE

Type: constant

Description: vst varmap manager


Replaced value:
```sqf
("__levst_cfg"+str __GLOB_CFG_IDX__+"_var_"+_var)
```
File: [client\LightEngine\VisualStatesConfigs.sqf at line 77](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L77)
## le_vst_create

Type: function

Description: initialize vst
- Param: _type
- Param: _src
- Param: _ctx

File: [client\LightEngine\VisualStatesConfigs.sqf at line 7](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L7)
## le_isVSTConfig

Type: function

Description: 


File: [client\LightEngine\VisualStatesConfigs.sqf at line 37](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L37)
## le_vst_remove

Type: function

Description: remove vst
- Param: _type
- Param: _src
- Param: _ctx

File: [client\LightEngine\VisualStatesConfigs.sqf at line 40](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L40)
## le_vst_createDummyObj

Type: function

Description: 
- Param: _model (optional, default "Sign_Sphere10cm_F")
- Param: _doHide (optional, default true)
- Param: _createAsVehicle (optional, default false)

File: [client\LightEngine\VisualStatesConfigs.sqf at line 63](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L63)
## le_vst_regVar

Type: function

Description: 
- Param: _obj
- Param: _var
- Param: _val

File: [client\LightEngine\VisualStatesConfigs.sqf at line 78](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L78)
## le_vst_hasVar

Type: function

Description: 
- Param: _obj
- Param: _var

File: [client\LightEngine\VisualStatesConfigs.sqf at line 82](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L82)
## le_vst_hasVarExt

Type: function

Description: 
- Param: _obj
- Param: _var
- Param: _cfg

File: [client\LightEngine\VisualStatesConfigs.sqf at line 85](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L85)
## le_vst_getVar

Type: function

Description: 
- Param: _obj
- Param: _var

File: [client\LightEngine\VisualStatesConfigs.sqf at line 90](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L90)
## le_vst_getVarExt

Type: function

Description: 
- Param: _obj
- Param: _var
- Param: _cfg

File: [client\LightEngine\VisualStatesConfigs.sqf at line 93](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L93)
## le_vst_remVar

Type: function

Description: 
- Param: _obj
- Param: _var

File: [client\LightEngine\VisualStatesConfigs.sqf at line 98](../../../Src/client/LightEngine/VisualStatesConfigs.sqf#L98)
# Bullets.sqf

## SHOT_BULLET_PISTOL_TIMEOUT

Type: constant

Description: 


Replaced value:
```sqf
0.25
```
File: [client\LightEngine\ShotableConfigs\Bullets.sqf at line 50](../../../Src/client/LightEngine/ShotableConfigs/Bullets.sqf#L50)
## SHOT_BULLET_SHOTGUN_TIMEOUT

Type: constant

Description: 


Replaced value:
```sqf
0.25
```
File: [client\LightEngine\ShotableConfigs\Bullets.sqf at line 91](../../../Src/client/LightEngine/ShotableConfigs/Bullets.sqf#L91)
## SHOT_BULLET_RIFLE_TIMEOUT

Type: constant

Description: 


Replaced value:
```sqf
0.25
```
File: [client\LightEngine\ShotableConfigs\Bullets.sqf at line 110](../../../Src/client/LightEngine/ShotableConfigs/Bullets.sqf#L110)
## le_internal_shot_bullet_loadLight

Type: function

Description: 
- Param: _intensity
- Param: _timeout

File: [client\LightEngine\ShotableConfigs\Bullets.sqf at line 7](../../../Src/client/LightEngine/ShotableConfigs/Bullets.sqf#L7)
## le_internal_shot_bullet_getFactPos

Type: function

Description: 
- Param: _addY (optional, default 0)

File: [client\LightEngine\ShotableConfigs\Bullets.sqf at line 32](../../../Src/client/LightEngine/ShotableConfigs/Bullets.sqf#L32)
# Stealth.sqf

## vst_human_stealth_allowStepsounds

Type: Variable

Description: 


Initial value:
```sqf
true
```
File: [client\LightEngine\VisualStates\Stealth.sqf at line 7](../../../Src/client/LightEngine/VisualStates/Stealth.sqf#L7)
