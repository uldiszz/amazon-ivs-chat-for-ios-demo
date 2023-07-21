source 'https://github.com/CocoaPods/Specs.git'

platform :ios, '14.0'

target 'SimpleChat' do
    pod 'AmazonIVSChat', '~> 1.0.0'
    pod 'AmazonIVSPlayer', '~> 1.20.0'
end

# Allow building for arm64e architecture, which AmazonIVSPlayer supports.
# See https://developer.apple.com/documentation/security/preparing_your_app_to_work_with_pointer_authentication
post_install do |installer|
    installer.pods_project.build_configurations.each do |configuration|
        configuration.build_settings['ARCHS[sdk=iphoneos*]'] = ['$(ARCHS_STANDARD)','arm64e']
    end
end