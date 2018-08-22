# illusion-excel
excel import and export for yii2

###example:

####export:
$cellData = [
            ['部门', '组别', '姓名', '性别'],
            ['一米技术部', 'oms', '周II', '男'],
            ['一米技术部', 'oms', '李kq', '男'],
            ['一米技术部', 'pms', 'w鑫', '女'],
        ];
        $excel = new excel\Excel();
        $fillData = $excel->export($cellData);
        $excel->download($fillData, 'test', 'Xls');
        
###import:
$excel = new excel\Excel($importFile->tempName);
$data = $excel->import(['belongTo', 'group', 'name', 'sex'], 'transform');
