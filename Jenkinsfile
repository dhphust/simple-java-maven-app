node () {
    stage('email'){
        echo "测试发送邮件"
        emailext(subject: '任务执行失败',to: 'enzohust@163.com',body: '''测试邮件内容...''')
    }
}
